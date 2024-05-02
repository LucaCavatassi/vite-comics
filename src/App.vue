<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";
  import AppFooterTop from "./components/AppFooterTop.vue"; 
  import AppFooterBottom from "./components/AppFooterBottom.vue";


  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooterTop,
      AppFooterBottom,
    },

    data() {
      return {

      }
    }
  }
</script>

<template>
  <div class="wrapper">
    <AppHeader />
    <AppMain />
    <AppFooterTop />
    <AppFooterBottom />
  </div>
</template>

<style lang="scss">
</style>