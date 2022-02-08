<template>

<div class="ms_container text-center">
    <h1>Best Seller</h1>
    <h6> Must have products from our top sellers</h6>
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