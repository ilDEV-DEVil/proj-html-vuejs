<template>
  <div class="d-flex justify-content-between w-100 text-white pt-3">
      <div class="imgContainer align-middle">
        <img class="" src="../assets/img/logo-restaurant-2x-200x38.png" alt="">
      </div>
      <ul class="d-flex list-unstyled align-content-center pt-2 pe-5 me-5" >
          <li class="px-3" v-for="item,i in linkList" :key="i">{{ item }}</li>
          <li><i class="fa fa-shopping-cart" aria-hidden="true"></i></li>
      </ul>
  </div>
</template>

<script>
export default {
name: "NavBar",
data(){
    return{
        linkList: [ "Home", "Culinary History", "Out Team", "Our Menu", "Takeout", "Bulletin", "Reservations",]
    }
}
}
</script>

<style lang="scss" scoped >

div{
    font-size: 15px;
    position: relative;
    img{
        position:absolute;
        left: 170px
    }
    ul{
        color: lightgray;
        font-size: 14px;
    }
    li{
        
        &:hover{
            color: white;
        }
    }
}

</style>