<template>
  <div id="app">
    <app-header />
    <app-main />
    <app-sponsor />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import AppSponsor from "./components/AppSponsor.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppSponsor,
  },
};
</script>

<style lang="scss">
@import "./style/general.scss";
#app {
  a {
    @include standard-a;
  }
  ul {
    @include standard-ul;
  }
}
</style>
