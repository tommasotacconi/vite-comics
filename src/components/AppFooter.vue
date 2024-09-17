<script>
import FooterTop from './FooterTop.vue'
import FooterBottom from './FooterBottom.vue'

export default {
  data() {
    return {
      
    }
  },
  components: {
    FooterTop,
    FooterBottom
  }
}
</script>

<template>
  <footer>
    <FooterTop />
    <FooterBottom />
  </footer>
</template>

<style lang="scss" scoped>
  footer {
    font-family: 'Open Sans Condensed';
  }
</style>