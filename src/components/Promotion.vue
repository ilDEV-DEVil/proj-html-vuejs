<template>
    <div class="mx-3">
        <img class="objectCover relative" :src="singlePromotion.src" alt="">
        <!-- <h4 class="absolute">{{ singlePromotion.title }}</h4> -->
        <h5 class="text-center pt-2">{{ singlePromotion.title }}</h5>
        <p class="text-center">{{ singlePromotion.text }}</p>
    </div>
</template>

<script>
export default {
name:"Promotion",
props: {
    singlePromotion : Object
}
}
</script>

<style lang="scss" scoped>
@import "../style/variable.scss";
div{

    transition: all .2s ease-in-out; 

    div:hover{
        transform: scale(1.1);
    }
}


img{
    width: 350px;
    height: 500px;
}
/* h4{
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 200px;
    color: white;
} */
h5{
font-family: 'Bebas Neue', cursive;

}

p{
    font-size: 10px;
}
</style>