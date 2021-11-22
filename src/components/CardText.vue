<template>
    <div class="CardText_container bg-black text-white d-flex justify-content-center align-items-center">
        <div class="containerText ">
            <div class="my_border"></div>
            <p>THE BEST RESTAURANT IN TOWN</p>
            <h1>FINE DINING EXPERIENCE </h1>
            <p class="mt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum a officiis dolorem, cupiditate voluptatem saepe aliquam, explicabo sit eaque molestiae, ipsa tenetur et excepturi accusantium? Ea sapiente pariatur et officia.</p>
            <button class="my_button mt-3">EXPLORE THE MENU</button>
        </div>
    </div>
</template>

<script>
export default {
name: "CardText",
}
</script>

<style lang="scss" scoped>
@import "../style/variable.scss";
.CardText_container{
    width: 45%;
    .containerText{
        max-width: 50%;
        position: relative;
        .my_border{
            border-top:1px solid white ;
            position: absolute;
            top: 7px;
            left: -40px;
            width: 25px;
        }
        p{
            font-size: 10px;
        }
        .my_button{
            @include blackButton
        }
    }
}
</style>