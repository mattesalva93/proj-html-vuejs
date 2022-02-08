<template>
<div class="text-center">
    <h1>New arrivals</h1>
    <h6> Brand new products from top designer</h6>
    <Carousel />
</div>


</template>


<script>
import Carousel from '../sub-components/Carousel.vue'
export default {
  components: { 
      Carousel 
      },

    name:"Bestseller"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';


</style>