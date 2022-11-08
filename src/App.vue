<script>
import AppHeader from "./components/AppHeader.vue"
export default{
  components: {
    AppHeader
  },

  data(){
    return{}
  }
}
</script>

<template>
  <AppHeader />

</template>

<style lang="scss">
@use './styles/general.scss' as *;
@use './styles/partials/variables' as *;
@use './styles/partials/mixins' as *;

</style>
