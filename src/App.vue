<template>
  <div id="app">
    <div class="header">
    <NavBar class="navBar"></NavBar>
    <TextImg :heroData="heroData[0]" class="mb-35 text-white bg-black"></TextImg>
    </div>
    <TextImg :heroData="heroData[1]" class="pb-35 text-black w-75 m-auto"></TextImg>
    
    

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
      heroData:[
        //DATA 0
        {
          src : require("@/assets/img/slider52x.jpg"),
          overTitle: "THE BEST TABLE IN TOWN",
          h1: "FINE DINING EXPERIENCE", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "EXPLORE THE MENU"
        },
        //DATA 1
        {
          src : require("@/assets/img/info22x.jpg"),
          overTitle: "ksdjskdjjkdsn",
          h1: "FOOD IS OUR COMMON GROUND, UNIVERSAL EXPERICENCE.", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          sign: require("@/assets/img/signature-200x172.jpg")
        },
      ]
    } 
  },
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "style/variable.scss";

.header{
  position: relative;
  .navBar{
    position: absolute;
    top:0
  }
}
</style>

//chiedere come inserire il percorso delle immagini senza doverle stampare ogni volta
