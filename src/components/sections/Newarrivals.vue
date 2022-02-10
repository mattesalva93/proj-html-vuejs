<template>
<div class="ms_carousel-container text-center">
  <div class="ms_container">
    <h2>New arrivals</h2>
  </div>
    <h6> Brand new products from top designer</h6>
    <div class="ms_model-carousel-container" id="carousel-container-2">
        <div v-for="(element, index) in modelliNewarrivals" 
          :key="index" 
          class="ms_carousel-img-container">
          <div class="ms_model-img">
            <img :src="element.src" alt="">
            <div class="ms_model-hover">
              <div>
                <p><b>{{element.modello}}</b></p>
                <span>{{element.tipologia}}</span>
                <p v-if="element.sconto != true">{{element.prezzo}}</p>
                <p v-else> <s>{{element.prezzo}}</s> {{element.prezzoscontato}} </p>
              </div>
              <div class="d-flex justify-content-around w-100">
                <div><i class="fas fa-shopping-cart"></i></div>
                <div><i class="fa-solid fa-list"></i> <span> Details </span></div>
              </div>
            </div>
          </div>
        </div>
    </div>
    <div @click="scrollaDestra" class="ms_carousel-buttons rx">
        <i class="fas fa-chevron-right"></i>
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
      position: relative;
      img{
      width: 100%;
      }
      .ms_model-hover{
        display: none;
        color: white;
      }
      &:hover .ms_model-hover{
        position: absolute;
        top:0;
        left: 0;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        height: 100%;
        width: 100%;
        background-image: linear-gradient($bluavada, $rosaavada);
        opacity: 0.9;
        cursor: pointer;
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