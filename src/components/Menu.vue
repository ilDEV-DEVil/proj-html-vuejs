<template>
  <div class="backgroundColor ps-5" :class="singleMenu.transform ? 'topTransform' : ''">
      <h4 class="pt-5 pb-5">{{ singleMenu.title }}</h4>
      <ul class="list-unstyled">
          <li v-for="singlePlate,i in singleMenu.plates" :key="i">
              <div class="d-flex justify-content-between">
                <h5 class="m-0">{{ singleMenu.plates[i].plateTitle }}</h5>
                <p  class="pe-5 me-2">{{ singleMenu.plates[i].platePrice }}</p>
              </div>
              <p class="pb-5 m-0 maxWidth"> {{ singleMenu.plates[i].plateDescription }} </p>
          </li>
      </ul>
  </div>
</template>

<script>
export default {
name:"Menu",
props:{
    singleMenu:Object
}

}
</script>

<style lang="scss" scoped>
.backgroundColor{
    background-color: rgb(214, 214, 214) ;
}
div{
    min-width: 350px;
    .topTransform{
        color: white;
        transform: translate(0 , -30px);
        background-image: url(".././assets/img/misc22x.jpg"), linear-gradient(rgb(0, 0, 0), rgb(141, 141, 141));
        background-size: 100% 100%;
        background-blend-mode: darken ,normal;

    }
}
p{
    font-size: 10px;
}
.maxWidth{
    max-width: 260px;
}
</style>