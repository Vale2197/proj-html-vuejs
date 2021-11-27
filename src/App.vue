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

html {
  scroll-behavior: smooth;
}
:root {
  --mainColor: #d2405d;
  }
  body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    min-width: 1440px;
     scroll-behavior: smooth;

        .imgColor {
            filter: hue-rotate(
            322deg) brightness(0.9);
        }
        
        .title {
          color:  #56509f;
        }

      
        .descr {
              color: grey;
        }
        

       .bgPurple {
              background-color: #56509f ;
        }

        .bgOrange {
          background-color: #d2405d ;
        }
  }
</style>
