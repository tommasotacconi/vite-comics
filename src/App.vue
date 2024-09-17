<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'
import "@fontsource/open-sans-condensed"

export default {
  data () {
    return {
    }
  },
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
    <AppHeader />
    <AppMain />
    <AppFooter />
</template>

<style lang="scss">
  @use 'bootstrap-icons/font/bootstrap-icons.scss';
  @use './styles/utilities.css' as *;
  @use './styles/general.scss' as *;

</style>
