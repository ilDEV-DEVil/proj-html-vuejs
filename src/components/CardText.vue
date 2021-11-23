<template>
    <div class="CardText_container d-flex justify-content-center align-items-center">
        <div class="containerText ">
            <p class="pt-1">{{ heroData.overTitle }}</p>
            <div class="containerTitle">
                <div class="my_border"></div>
                <h1 class="">{{heroData.h1}}</h1>
            </div>
            <p class="mt-3">{{ heroData.text }}</p>
            <button class="my_button mt-3" v-if="heroData.buttonText" >{{ heroData.buttonText }}</button>
            <img class="w-25" v-if="heroData.sign" :src="heroData.sign" alt="">
        </div>
    </div>
</template>

<script>
export default {
name: "CardText",
props:{
    heroData: Object
}
}
</script>

<style lang="scss" scoped>
@import "../style/variable.scss";
.CardText_container{
    width: 35%;
    .containerText{
        max-width: 50%;
        p{
            font-size: 10px;
        }

        .containerTitle{
            position:relative;
            display: inline-block;

            .my_border{
                border-top:1px solid white ;
                position: absolute;
                top: 25px;
                left: -70px;
                width: 40px;
            }
            
        }
    }
}
.my_button{
 @include blackButton

}
</style>