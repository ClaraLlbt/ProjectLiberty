<template>
  <div id="app">
    <router-view to="/"/> 
  </div>
</template>

<script>
import ComponentWithMap from './components/GoogleMaps.vue'
import WhoIAm from "./components/whoIAm.vue";
export default {
  name: "App",
  components: {
    WhoIAm,
    ComponentWithMap,
  },
};
</script>

<style lang="scss">
html {
  height: 100%;
}
body {
  min-height: 100%;
  width: 100%;
}
#home {
  min-height: 100vh;
}
</style>
