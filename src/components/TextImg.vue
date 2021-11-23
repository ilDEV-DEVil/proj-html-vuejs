<template>
  <div class="d-flex my_container">
    
    <CardText :heroData="heroData" ></CardText>
    <div class="containerImg">    
        <img :src= "heroData.src"  alt="">
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
    height: 510px;
    .containerImg{
        width: 55%;
        height: 100%;
        img{
            height: 100%;
            width:100%
        }
    }
}

</style>