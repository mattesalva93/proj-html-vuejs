<template>

<div class="ms_carousel-container ms_container text-center">
    <h1>Best Sellers</h1>
    <h6> Brand new products from top designer</h6>
    <div @click="scrollaDestra" class="ms_carousel-buttons rx">
        <i class="fas fa-chevron-right"></i>
    </div>
    <div class="ms_model-carousel-container" id="carousel-container-1">
        <div v-for="(element, index) in modelliBestSellers" 
          :key="index" 
          class="ms_carousel-img-container">
          <img :src="element.src" alt="">
        </div>
    </div>
    <div @click="scrollaSinsitra" class="ms_carousel-buttons lx">
        <i class="fas fa-angle-left" ></i>
    </div>
</div>

</template>


<script>
import products from '../data/avada.js';

export default {

  name:"Bestseller",
  data(){
    return{
      modelli: products,
      modelliBestSellers: [],
    }
  },
  created (){
    this.getBestSeller();
  },
  methods: {
    getBestSeller (){
      this.modelliBestSellers = this.modelli.filter(element => element.bestseller);
    },
    scrollaDestra(){
      document.getElementById('carousel-container-1').scrollLeft += 256;
    },
    scrollaSinsitra(){
      document.getElementById('carousel-container-1').scrollLeft -= 256;
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
  .ms_model-carousel-container{
    display: flex;
    flex: 0 0 auto;
    width: 100%;
    overflow-x: auto;
    &::-webkit-scrollbar {
    display: none;
  }
    .ms_carousel-img-container{
      min-width: 20%;
      img{
      width: 100%;
      }
      }
    }

  .ms_carousel-container{
    position: relative;
    .ms_carousel-buttons{
      position: absolute;
      top: 50%;
      padding: 10px 6px;
      background-color: lightgrey;
      color: white;
      font-size: 0.8rem;
  }
  .lx{
      left: 1%;
  }
  .rx{
      right: 1%;
  }
  }
</style>