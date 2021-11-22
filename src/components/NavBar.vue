<template>
  <div class="d-flex justify-content-between container fixed-top text-white pt-3">
      <div class="imgContainer align-middle">
        <img class="ps-5" src="../assets/img/logo-restaurant-2x-200x38.png" alt="">
      </div>
      <ul class="m-0 d-flex list-unstyled align-content-center pt-2" >
          <li class="px-3" v-for="item,i in linkList" :key="i">{{ item }}</li>
      </ul>
  </div>
</template>

<script>
export default {
name: "NavBar",
data(){
    return{
        linkList: [ "Home", "Culinary History", "Out Team", "Our Menu", "Takeout", "Bulletin", "Reservations", "spesa"  ]
    }
}
}
</script>

<style lang="scss" scoped >

div{
    font-size: 11px;
    ul{
        color: lightgray;
    }
    li{
        
        &:hover{
            color: white;
        }
    }
}

</style>