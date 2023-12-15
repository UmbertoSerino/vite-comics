<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from "./components/AppFooter.vue";

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template lang="">
  <AppHeader />
  <AppMain />
  <AppFooter />
</template>

<style lang="scss">
@use './style/general.scss' as*;
@use '../node_modules/@fortawesome/fontawesome-free/scss/solid.scss' as*;
@use '../node_modules/@fortawesome/fontawesome-free/scss/fontawesome.scss' as*
</style>
