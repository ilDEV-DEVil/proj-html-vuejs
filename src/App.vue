<template>
  <div id="app">
    <!-- 1 -->
    <div class="header pb-35">
      <NavBar class="navBar"></NavBar>
      <TextImg :heroData="heroData[0]" class="mb-35 text-white bg-black containerOne "></TextImg>
    </div>

    <!-- 2 -->
    <TextImg :heroData="heroData[1]" class="pb-35 text-black containerTwo justify-content-center"></TextImg>


    <!-- 3 -->
    <div class="d-flex justify-content-center pt-35 pb-35">
      <RestaurantInfo v-for="singleInfo,i in menuInfoData" :key="i" :menuInfoData="menuInfoData[i]" class="row"></RestaurantInfo>
    </div>
    
    <!-- 4 -->
    <TextImg :heroData="heroData[2]" class="flex-row-reverse bg-black text-white mt-35 mb-35 containerOne" ></TextImg>

    <!-- 5 -->
    <TextImg :heroData="heroData[3]" class="pb-35 pt-35 text-white containerTwo justify-content-center flex-row-reverse"></TextImg>

    <div class="containerTwo d-flex justify-content-center">
      <!-- <div class="articleImg me-1">
        <img src="@/assets/img/info52x.jpg" alt="">
      </div>
      <div class="articleImg ms-1">
        <img src="@/assets/img/info22x.jpg" alt="">  
      </div> -->
      <CardText class="articleBackgroundDx" :heroData="heroData[4]"></CardText>
      <CardText :heroData="heroData[5]"></CardText>

    </div>

  </div>
</template>


   
<script>

import TextImg from "./components/TextImg.vue"
import NavBar from "./components/NavBar.vue"
import RestaurantInfo from "./components/RestaurantInfo.vue"
import CardText from "./components/CardText.vue"



export default {
  name: 'App',
  components: { TextImg, NavBar, RestaurantInfo, CardText},
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
          overTitle: ", alias harum quae, eum velit maxime. Ullam maiores, voluptate sit eos quisquam natus accusamus cumque!",
          h1: "FOOD IS OUR COMMON GROUND, UNIVERSAL EXPERICENCE.", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          sign: require("@/assets/img/signature-200x172.jpg"),
          smallImg: true

        },
         //DATA 2
        {
          src : require("@/assets/img/slider32x.jpg"),
          overTitle: "FINE DINING EXPERIENCE",
          h1: "THE BEST TABLE IN TOWN.", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "EXPLORE THE MENU"
          
        },
         //DATA 3
        {
          src : require("@/assets/img/blog72x-1200x1375.jpg"),
          overTitle: "FINE DINING EXPERIENCE",
          h1: "THE BEST TABLE IN TOWN.", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "EXPLORE THE MENU",
          smallImg: true,
          smallImgBlack: true
        },
        //DATA 4
        {
          overTitle: "",
          h1: "THE GUARDIAN", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "EXPLORE THE MENU",
          smallImg: true,
          smallImgBlack: true
        },
        //DATA 5
        {
          overTitle: "",
          h1: "GLOBE AND MAIL", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "EXPLORE THE MENU",
          smallImg: true,
          smallImgBlack: true
        },
      ],

      menuInfoData:[
        //DATA 0
        {
          src: require("@/assets/img/sushi-1.png") ,
          title: "THE BEST TABLE IN TOWN" ,
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aspernatur minus ad autem omnis quibusdam ea, alias harum quae, eum velit maxime. Ullam maiores, voluptate sit eos quisquam natus accusamus cumque!" ,
          buttonText: "EXPLORE THE MENU" ,
        },

        //DATA 1
        {
          src: require("@/assets/img/sushi-2.png") ,
          title: "THE BEST TABLE IN TOWN" ,
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aspernatur minus ad autem omnis quibusdam ea, alias harum quae, eum velit maxime. Ullam maiores, voluptate sit eos quisquam natus accusamus cumque!" ,
          buttonText: "EXPLORE THE MENU" ,
        },

        //DATA 2
        {
          src: require("@/assets/img/sushi-3.png") ,
          title: "THE BEST TABLE IN TOWN" ,
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aspernatur minus ad autem omnis quibusdam ea, alias harum quae, eum velit maxime. Ullam maiores, voluptate sit eos quisquam natus accusamus cumque!" ,
          buttonText: "EXPLORE THE MENU" ,
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

.containerTwo{
    .articleImg{
      width: 520px;
      .articleBackgroundDx{
        background-image: url("./assets/img/info52x.jpg");
      }
      /* img{
        height: 100%;
        width: 100%;
      } */
    }
}

</style>

//chiedere come inserire il percorso delle immagini senza doverle stampare ogni volta
//inserire la background img riga 159 non viene presa la classe articleImg