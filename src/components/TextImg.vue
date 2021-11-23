<template>
  <div class="d-flex my_container">
    
    <CardText :class="heroData.smallImgBlack ? 'bg-black' : ''" :heroData="heroData" ></CardText>
    <div class="containerImg col-6" :class="heroData.smallImg  ? 'smallImg' : ''">    
        <img  :src= "heroData.src"  alt="">
    </div>   

  </div>
</template>

<script>

import CardText from "./CardText.vue"

export default {
name: "TextImg",
components: { CardText, },
props: {
    heroData: Object,
    }
}
</script>

<style lang="scss" >
.my_container{
    width: 100%;
    .containerImg{
        width: 65%;
        height: 100%;
        img{
            height: 100%;
            width:100%;
            object-fit: cover;
        }
    }
}
.smallImg{
    width: 525px !important;


}

</style>