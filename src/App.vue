<script>
import AppHeader from "./components/AppHeader.vue";
export default {
  
  components: {
    AppHeader
  },

  data() {
    return {

    }
  }
}
</script>

<template>
<AppHeader />
</template>

<style lang="scss">
@use './style/general.scss' as *;
@use './style/partials/variables.scss' as *;
@use './style/partials/mixins.scss' as *;
@use '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
