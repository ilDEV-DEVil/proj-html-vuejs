<template>
    <div class="infoContainer d-flex flex-column align-items-center mx-5">
        <div class="d-flex flex-column align-items-center ">
            <div class="imgContainer"><img class="" :src="menuInfoData.src" alt=""></div>
            <h6 class="mt-2 mb-4 text-center">{{ menuInfoData.title }}</h6>
            <p class="fontSize text-center">{{ menuInfoData.text }}</p>
        </div>
        <button class="fontSize">{{ menuInfoData.buttonText }}</button>
    </div>
</template>

<script>
export default {
name:"RestaurantInfo",
props:{ 
    menuInfoData : Object
 }

}
</script>

<style lang="scss" scoped>
@import "../style/variable.scss";
.infoContainer{
    max-width: 250px;
    .imgContainer{
        width: 80px;
        height: 60px;
        img{
            height: 100%;
            width: 100%;
        }
    }
    .fontSize{
        font-size: 10px;
    }
    button{
        @include whiteButton
    }
    h6{
        font-family: 'Bebas Neue', cursive;
    }

}
</style>