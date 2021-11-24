<template>
    <div class="mx-3">
        <img class="objectCover" :src="singlePromotion.src" alt="">
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
img{
    width: 350px;
    height: 500px;
}
h5{
font-family: 'Bebas Neue', cursive;

}

p{
    font-size: 10px;
}
</style>