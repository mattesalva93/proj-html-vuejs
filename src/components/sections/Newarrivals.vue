<template>
<div class="text-center">
    <h1>New arrivals</h1>
    <h6> Brand new products from top designer</h6>
    <div class="ms_model-carousel-container">
        <div class="ms_carousel-buttons rx">
            <i class="fas fa-chevron-right"></i>
        </div>
        <img 
        v-for="(element, index) in modelliBestSellers" 
        :key="index"
        :src="element.src" alt=""
        class="ms_carousel-off"
        :class="{'ms_carousel-active': getIndiceAttivo(index)}" />
        <div class="ms_carousel-buttons lx">
            <i class="fas fa-angle-left"></i>
        </div>
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
    getIndiceAttivo (indice){
      if(indice <= 4){
        return true
      }
      else{
        return false
      }
    },
  }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

.ms_model-carousel-container{
        position: relative;
        img{
            width: 20%;
        }
        .ms_carousel-off{
          display: none;
        }
        .ms_carousel-active{
          display: inline-block;
        }
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