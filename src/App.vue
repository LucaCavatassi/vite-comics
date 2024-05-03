<script>
  import AppHeader from "./components/AppHeader.vue";
  import AppHero from "./components/AppHero.vue"
  import AppMain from "./components/AppMain.vue";
  import AppFooterTop from "./components/AppFooterTop.vue"; 
  import AppFooterBottom from "./components/AppFooterBottom.vue";
  import AppSocials from "./components/AppSocials.vue";


  export default {
    components: {
      AppHeader,
      AppHero,
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
      <AppHero />
      <AppMain />
      <AppFooterTop />
      <AppFooterBottom />
      <AppSocials />
    </div>
  </div>
</template>

<style lang="scss">
</style>