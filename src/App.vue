<script>
  import AppHeader from './components/AppHeader.vue';
  import AppContent from './components/AppContent.vue';
  import AppLinks from './components/AppLinks.vue';
  import AppFooterTop from './components/AppFooterTop.vue';
  import AppFooterBottom from './components/AppFooterBottom.vue';


  export default {
    data () {
      return {

      }
    },
    
    components: { AppHeader , AppContent, AppLinks, AppFooterTop, AppFooterBottom},

  }

</script>

<template>
    <AppHeader></AppHeader>

    <AppContent></AppContent>

    <AppLinks></AppLinks>

    <AppFooterTop></AppFooterTop>

    <AppFooterBottom></AppFooterBottom>
</template>


<style lang="scss">
  @use './assets/styles/general.scss' as *;


</style>
