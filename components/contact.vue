<template lang='pug'>
// v-layout(justify-center)
    // v-flex(lg6).red
        // v-card
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
            new contact 'Téléphone', 'phone', ['06 ** ** ** **', '', '02 ** ** ** **']
            new contact 'Mail', 'email', ['camille-giraud@***']
            new contact 'Addresse', 'home', ["11 Rue ***", "*** sur ***", "27*** *** *** d'***"]
        ]
        active: null
</script>