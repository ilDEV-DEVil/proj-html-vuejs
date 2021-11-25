<template>
  <div id="app">
    <!-- heroData 1 -->
    <div class="header pb-35">
      <NavBar class="navBar"></NavBar>
      <TextImg :heroData="heroData[0]" class="mb-35 text-white bg-black containerOne "></TextImg>
    </div>

    <!-- heroData 2 -->
    <TextImg :heroData="heroData[1]" class="pb-35 text-black containerTwo justify-content-center"></TextImg>


    <!-- heroData 3 -->
    <div class="d-flex justify-content-center pt-35 pb-35">
      <RestaurantInfo v-for="singleInfo,i in menuInfoData" :key="i" :menuInfoData="menuInfoData[i]" class="row"></RestaurantInfo>
    </div>
    
    <!-- heroData 4 -->
    <TextImg :heroData="heroData[2]" class="flex-row-reverse bg-black text-white mt-35 mb-35 containerOne" ></TextImg>

    <!-- heroData 5 -->
    <h3 class="text-center pt-35"><em>What critics say about us</em></h3>
    <TextImg :heroData="heroData[3]" class="pb-35 pt-35 text-white containerTwo justify-content-center flex-row-reverse"></TextImg>

    <div class="containerTwo d-flex justify-content-center pt-35 pb-35">
      <CardText class="articleBackgroundDx text-white" :heroData="heroData[4]"></CardText>
      <CardText class="articleBackgroundSx text-white" :heroData="heroData[5]"></CardText>
    </div>

   
    <img class="imgHero pt-35 mb-35" src="./assets/img/page52x.jpg" alt="">
  
    <h3 class="text-center pt-35"><em>Latest news and promotions</em></h3>

    <div class="d-flex pt-35 justify-content-center pb-35"> 
      <Promotion v-for="singlePromotion,i in promotionData" :key="i" :singlePromotion="singlePromotion"> </Promotion>
    </div>

    <!-- heroData 6 -->
    <TextImg :heroData="heroData[6]" class="flex-row-reverse bg-black text-white mt-35 mb-35 containerOne" ></TextImg>
    
    <div class="d-flex justify-content-center pt-35 pb-35">
      <Menu v-for="singleMenu,i in menuPlatesData" :key="i" :singleMenu="singleMenu"></Menu>
    </div>

  <!-- heroData 7 -->
    <div class="containerOne mt-35 relative">
      <img class="w-100 h-100 objectCover" src="./assets/img/hero42x.jpg" alt="">
      <!-- <CardText class="bg-black text-white mw-25 absolute" :heroData="heroData[7]"></CardText> -->
    </div>

    <div class="footer">
      <div class="footerContainerImg"><img class="w-100 h-100" src="./assets/img/logo-restaurant.png" alt=""></div>
      <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. </p>
      <ul class="list-unstyled d-flex">
        <li v-for="singleIcon,i in socialList" :key="i" class="px-1"><i class="fa" :class="socialList[i]" aria-hidden="true"></i></li>
      </ul>
    </div>

  </div>
</template>


   
<script>

import TextImg from "./components/TextImg.vue"
import NavBar from "./components/NavBar.vue"
import RestaurantInfo from "./components/RestaurantInfo.vue"
import CardText from "./components/CardText.vue"
import Promotion from "./components/Promotion.vue"
import Menu from "./components/Menu.vue"




export default {
  name: 'App',
  components: { TextImg, NavBar, RestaurantInfo, CardText, Promotion, Menu},
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
          overTitle: "MEGGY STEWART",
          h1: "NEW YORK TIMES", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "READ THE FULL ARTICLE",
          smallImg: true,
          smallImgBlack: true
        },
        //DATA 4
        {
          overTitle: "",
          h1: "THE GUARDIAN", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "READ THE FULL ARTICLE",
          smallImg: true,
          smallImgBlack: true
        },
        //DATA 5
        {
          overTitle: "",
          h1: "GLOBE AND MAIL", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "READ THE FULL ARTICLE",
          smallImg: true,
          smallImgBlack: true
        },
        //DATA 6
        {
          src : require("@/assets/img/slider72x-scaled.jpg"),
          overTitle: "ENJOY YOUR MEAL AT HOME",
          h1: "GLOBE AND MAIL", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh",
          buttonText: "VIEW TAKEOUT MENU",
          
        },
         //DATA 7
        {
          overTitle: "",
          h1: "BRAISED ABALONE", 
          text:"lorem ipsum ahahahchjskjsdjbgvghfghjfjabsxjas xasjhuasxhsaxhkjh ffffffffffffffffffffffffffffffffffffffffffffff",
          buttonText: "VIEW IN THE MENU",
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
          title: "PERFECT FOR GROUP" ,
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aspernatur minus ad autem omnis quibusdam ea, alias harum quae, eum velit maxime. Ullam maiores, voluptate sit eos quisquam natus accusamus cumque!" ,
          buttonText: "MAKE A RESERVATION" ,
        },

        //DATA 2
        {
          src: require("@/assets/img/sushi-3.png") ,
          title: "FRESH PRODUCE EVERYDAY" ,
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aspernatur minus ad autem omnis quibusdam ea, alias harum quae, eum velit maxime. Ullam maiores, voluptate sit eos quisquam natus accusamus cumque!" ,
          buttonText: "LEARN MORE ABOUT US" ,
        },
      ],

      promotionData:[
        {
          src: require("@/assets/img/blog92x.jpg"),
          title: "THE BEST COFEE IN TOWN",
          text: "By admin | January 7th, 2020 | Categeries: News",
        },
        {
          src: require("@/assets/img/blog72x.jpg"),
          title: "DISCOVER OUR NEW MENU",
          text: "By admin | January 7th, 2020 | Categeries: News",
        },
        {
          src: require("@/assets/img/blog82x.jpg"),
          title: "WE NOW ACCEPT SQUARE!",
          text: "By admin | January 7th, 2020 | Categeries: News",
        },
      ],

      menuPlatesData:[
        {
          title:"HORS D'OEUVRES",
          plates: [
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"UMI MASU SALAD",
              platePrice:"$21",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"TEMAKI WITH CRAB",
              platePrice:"$32",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"CALIFORNIA ROLLS",
              platePrice:"$22",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
          ]
        },
        {
          title:"MAIN COURSE",
          transform: true,
          plates: [
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
             plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
          ]
        },
        {
          title:"DESSERTS",
          plates: [
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
            {
              plateTitle:"AHI SALMON NIGIRI",
              platePrice:"$48",
              plateDescription:"Eget vulputater vitae quis rutrum blanditsed. Quam nulla sit lacinia",
            },
          ]
        },
      ],

      socialList:[  "fa-facebook","fa-twitter","fa-youtube-play","fa-instagram","fa-linkedin" ],
    } 
  },
}
</script>

<style lang="scss">
@import "~bootstrap/scss/bootstrap";
@import "style/variable.scss";
@import "~font-awesome/css/font-awesome.min.css";
@import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Lora:ital@0;1&family=Work+Sans:wght@300;400&display=swap');

h1{
font-family: 'Bebas Neue', cursive;
}
p,h3{
  font-family: 'Lora', serif;
  
}
.header{
  position: relative;
  .navBar{
    position: absolute;
    top:0
  } 
}

.articleBackgroundDx{
        background-image: url("./assets/img/info52x.jpg"), linear-gradient(black, rgba(255, 255, 255, 0.363));
        background-size: 100% 100%;      
        background-blend-mode: darken ,luminosity;

}

.articleBackgroundSx{
        background-image: url("./assets/img/info12x.jpg"),  linear-gradient(black, rgba(255, 255, 255, 0.89));
        background-size: 100% 100%;
        background-blend-mode: darken ,luminosity;
       
}

.imgHero{
  width: 100%;
  height: 500px; 
}

.footer{
  background-image: url("./assets/img/footer2x.jpg");
  width: 100%;
  height: 50vh;
  background-size: 100% 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  .footerContainerImg{
    width: 200px;
    
  }
  p{
    margin-top: 30px;
    color: white;
  }
  i{
    //bg-white text-dark
    background-color: white;
    color: black;
    height: 25px;
    width: 25px;
    border-radius: 50%;
    text-align: center;
    line-height: 25px;
  }
}

</style>

//chiedere come inserire il percorso delle immagini senza doverle stampare ogni volta
// inserire e commerciale nei testi