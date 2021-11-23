<template>
  <div id="app">
    <NavBar></NavBar>
    <TextImg class="pb-35"></TextImg>
    
    

  </div>
</template>

<script>

import TextImg from "./components/TextImg.vue"
import NavBar from "./components/NavBar.vue"


export default {
  name: 'App',
  components: { TextImg, NavBar},
  data(){
    return{
      
    } 
  },
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "style/variable.scss"
</style>
