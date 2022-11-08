<script>
import AppHeader from "./components/AppHeader.vue"
import MainContent from "./components/MainContent.vue"
export default{
  components: {
    AppHeader,
    MainContent
  },

  data(){
    return{}
  }
}
</script>

<template>
  <AppHeader />
  <MainContent />

</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;
@use './styles/partials/mixins' as *;

</style>
