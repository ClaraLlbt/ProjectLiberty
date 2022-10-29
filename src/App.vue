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
  body {
    min-height: 100%;
    width: 100%;
    overflow-x: hidden;
    #app {
      font-family: "Source Code Pro", monospace;
      max-width: 95vw;
      @media (max-width: 1024px ){
        padding: 0;
      }
    }
  }
}
</style>
