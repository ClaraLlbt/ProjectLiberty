<template>
  <div id="">
    <router-view to="/"/> 
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style lang="scss">
html {
  height: 100%;
  overflow-x: hidden;
}
body {
  min-height: 100%;
  width: 100%;
}
#app {
  font-family: "Source Code Pro", monospace;
  width: 100%;
}
</style>
