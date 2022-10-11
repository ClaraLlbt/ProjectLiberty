<template>
  <div id="app">
    <router-view to="/"/> 
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style scopedlang="scss">
html {
  height: 100%;
  overflow-x: hidden;
}
body {
  min-height: 100%;
  width: 100%;
}
</style>
