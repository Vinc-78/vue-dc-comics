<template>
  <div id="app">
    <header><Header></Header></header>
    <main><Main></Main></main>
    <footer> <Footer></Footer> </footer>
  
    
  </div>
</template>

<script>

import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue"


export default {
  name: 'App',
  components: {

    Header,
    Main,
    Footer
    
    
    
  }
}
</script>

<style lang="scss">

@import "styles/Variables";
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  
}

</style>
