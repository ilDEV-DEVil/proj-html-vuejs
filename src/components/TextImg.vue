<template>
  <div class="d-flex my_container">
    
    <CardText></CardText>
    <div class="containerImg">    
        <img src="@/assets/img/slider52x.jpg"  alt="">
    </div>   

  </div>
</template>

<script>

import CardText from "./CardText.vue"

export default {
name: "TextImg",
components: { CardText, },
/* props: {
    imgSrc : String,
    }
 */}
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