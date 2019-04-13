<template lang='pug'>
div
  bandeau
  contact
  v-parallax(src='/jardin2.jpg')
  texte
  v-parallax(src='/jardin3.jpg')
</template>

<script lang='coffee'>
import contact from '~/components/contact'
import bandeau from '~/components/bandeau'
import texte from '~/components/texte'
export default
  components: {contact, bandeau, texte}
</script>