<template>
    <div class="CardText_container d-flex justify-content-center align-items-center" >
        <div class="containerText ">
            
            <div class="containerTitle">
                <div class="my_border"></div>
                <p class="pt-1 overTitle">{{ heroData.overTitle }}</p>
            </div>
            
            <h1 class="">{{heroData.h1}}</h1>
            <p class="mt-3">{{ heroData.text }}</p>
            <button class="my_button mt-3 overTitle" v-if="heroData.buttonText" >{{ heroData.buttonText }}</button>
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
    transition: all .2s ease-in-out; 
    &:hover{
        transform: scale(1.1);
    }
    
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
                top: 11px;
                left: -66px;
                width: 40px;
            }
            
        }
    }
}
.overTitle{
    font-family: 'Work Sans', sans-serif;
}
.my_button{
    @include blackButton;
    &:hover{
        @include whiteButton
    }
   
}
</style>