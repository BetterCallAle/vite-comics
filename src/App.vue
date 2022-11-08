<script>
import AppHeader from "./components/AppHeader.vue";
import MainContent from "./components/MainContent.vue";
import ShopNav from "./components/ShopNav.vue"
import AppFooter from "./components/AppFooter.vue"

export default{
  components: {
    AppHeader,
    MainContent,
    ShopNav,
    AppFooter
  },

  data(){
    return{}
  }
}
</script>

<template>
  <AppHeader />
  
  <main>
    <MainContent />
    <ShopNav />
  </main>

  <AppFooter />

</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;
@use './styles/partials/mixins' as *;

</style>
