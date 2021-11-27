<template>
  <div id="app">

    <siteHeader/>
    <!-- 
       / HEADER
     -->

    <siteMain/>
    <!-- 
       / MAIN
     -->

    <siteFooter/>
    <!-- 
        / FOOT.
     -->

  </div>
</template>

<script>
import siteHeader from "./components/siteHeader.vue";
import siteMain from "./components/siteMain.vue";
import siteFooter from "./components/siteFooter.vue";

export default {
  name: 'App',
    components: {
      siteHeader,
      siteMain,
      siteFooter,
    }
  
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap";
  body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    min-width: 1440px;
  }
</style>
