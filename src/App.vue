<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppMain from "./components/AppMain.vue";
  import AppFooterTop from "./components/AppFooterTop.vue"; 
  import AppFooterBottom from "./components/AppFooterBottom.vue";
  import AppSocials from "./components/AppSocials.vue";


  export default {
    components: {
      AppHeader,
      AppMain,
      AppFooterTop,
      AppFooterBottom,
      AppSocials,
    },

    data() {
      return {

      }
    }
  }
</script>

<template>
  <div class="big-wrapper">
    <div>
      <AppHeader />
      <AppMain />
      <AppFooterTop />
      <AppFooterBottom />
      <AppSocials />
    </div>
  </div>
</template>

<style lang="scss">
</style>