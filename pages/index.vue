<template lang='pug'>
div
  bandeau
  contact
  v-parallax(src='/jardin2.jpg')
  texte
  v-parallax(src='/jardin3.jpg')
  // v-list
    v-list-tile 51 54 5 54 54
    v-divider
    v-list-tile 51 54 5 54 54
</template>

<script lang='coffee'>
import contact from '~/components/contact'
import bandeau from '~/components/bandeau'
import texte from '~/components/texte'
export default
  components: {contact, bandeau, texte}
</script>