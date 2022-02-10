<template>
<div class="ms_carousel-container text-center">
  <div class="ms_container">
    <h2>New arrivals</h2>
  </div>
    <h6> Brand new products from top designer</h6>
    <div @click="scrollaDestra" class="ms_carousel-buttons rx">
        <i class="fas fa-chevron-right"></i>
    </div>
    <div class="ms_model-carousel-container" id="carousel-container-2">
        <div v-for="(element, index) in modelliNewarrivals" 
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
  name:"Newarrivals",
    data(){
    return{
      modelli: products,
      modelliNewarrivals: [],
    }
  },
  created (){
    this.getBestSeller();
  },
  methods: {
    getBestSeller (){
      this.modelliNewarrivals = this.modelli.filter(element => element.bestseller);
    },
    scrollaDestra(){
      document.getElementById('carousel-container-2').scrollLeft += 509;
    },
    scrollaSinsitra(){
      document.getElementById('carousel-container-2').scrollLeft -= 509;
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
    h6{
      margin-bottom: 35px;
      color: $grigioavada;
    }

  .ms_carousel-container{
    position: relative;
    padding: 100px 0;
    .ms_carousel-buttons{
      position: absolute;
      top: 50%;
      padding: 20px 10px;
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
h2{
    display: flex;
    justify-content: center;
    align-items: center;
    &:after{
        content: '';
        flex: 1;
        margin-left: 1rem;
        height: 1px;
        background-color: $bordiavada;
    }
    &:before{
        content: '';
        flex: 1;
        margin-right: 1rem;
        height: 1px;
        background-color: $bordiavada;
    }
  }

</style>