<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },

  data() {
    return {

    }
  }
}
</script>

<template>
<AppHeader/>
<AppMain/>
<AppFooter/>
</template>

<style lang="scss">
@use './style/general.scss' as *;
@use './style/partials/variables.scss' as *;
@use './style/partials/mixins.scss' as *;
@use '../node_modules/bootstrap/scss/bootstrap.scss';
</style>
