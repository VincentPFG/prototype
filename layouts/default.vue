<template lang='pug'>
v-app(:dark='dark')
    v-toolbar(app).primary
        v-toolbar-title Camille GIRAUD
        v-spacer
        v-toolbar-items
            v-btn(flat icon @click='dark=!dark')
                v-icon(v-if='dark') brightness_5
                v-icon(v-else) brightness_2
    v-content
        // v-container
        nuxt
    v-footer(app absolute).primary
        v-layout
            v-flex(text-xs-center) Developed by #[strong Vincent GIRAUD]
</template>

<script lang='coffee'>
export default
    data: ->
        dark: off
</script>