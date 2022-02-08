<template>

<div class="ms_container text-center">
    <h1>New arrivals</h1>
    <h6> Brand new products from top designer</h6>
    <div class="ms_model-carousel-container">
        <div class="ms_carousel-buttons rx">
            <i class="fas fa-chevron-right"></i>
        </div>
        <Model-pic 
        v-for="(element, index) in 5" :key="index"/>
        <div class="ms_carousel-buttons lx">
            <i class="fas fa-angle-left"></i>
        </div>
    </div>
</div>

</template>


<script>
import ModelPic from '../sub-components/Model-pic.vue'
export default {
  components: { 
      ModelPic 
    },
    name:"Bestseller"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_model-carousel-container{
        position: relative;
        img{
            width: 20%;
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
            left: 0;
        }
        .rx{
            right: 0;
        }
    }

</style>