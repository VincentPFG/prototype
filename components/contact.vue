<template lang='pug'>
v-layout(justify-center)
    // v-flex(lg6)
    //     v-toolbar
    //         v-toolbar-title Contacter
    //         // template(v-slot:extension)
    //     v-tabs(
    //         v-model='active' 
    //         icons-and-text
    //         centered
    //     )
    //         v-tab(v-for='contact in contacts') {{contact.name}}
    //             v-icon {{contact.icon}}
    //     v-tabs-items(v-model='active')
    //         v-tab-item(v-for='contact in contacts').text-xs-center.headline
    //             v-card(flat)
    //                 v-card-text
    //                     template(v-for='part in contact.content') {{part}} #[br]


    // v-flex(lg6)
    //     v-toolbar
    //         v-toolbar-title Contacter
    //         // template(v-slot:extension)
    //         v-tabs(
    //             v-model='active' 
    //             centered
    //             icons-and-text
    //             slot='extension'
    //         )
    //             v-tab(v-for='contact in contacts') {{contact.name}}
    //                 v-icon {{contact.icon}}
    //     v-tabs-items(v-model='active')
    //         v-tab-item(v-for='contact in contacts').text-xs-center.headline
    //             v-card
    //                 v-card-text
    //                     template(v-for='part in contact.content') {{part}} #[br]

    v-flex(lg6)
        v-card
            v-tabs(
                v-model='active' 
                icons-and-text
                centered
            )
                v-tab(v-for='contact in contacts') {{contact.name}}
                    v-icon {{contact.icon}}
            v-tabs-items(v-model='active')
                v-tab-item(v-for='contact in contacts').text-xs-center.headline
                    v-card(flat)
                        v-card-text
                            template(v-for='part in contact.content') {{part}} #[br]
</template>

<script lang='coffee'>
class contact
    constructor: (@name, @icon, @content) ->
export default
    data: ->
        contacts: [
            new contact 'Téléphone', 'phone', ['06 70 13 08 03', '02 32 34 66 56']
            new contact 'Mail', 'email', ['camille-giraud@live.fr']
            new contact 'Addresse', 'home', ["11 Rue des Longines", "Écardenville sur Eure", "27490 CLEF Vallée d'Eure"]
        ]
        active: null
        # text: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.'
</script>