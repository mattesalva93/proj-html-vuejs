<template>
<div class="ms_container text-center">
    <h2>Featured Products </h2>
    <h6>Must have products from our top sellers</h6>
    <div class="ms_products-target">
        Men
    </div>
    <div class="ms_products-target">
        Women
    </div>
    <div class="ms_products-target">
        Accessories
    </div>
    <Model />
</div>
</template>

<script>
import Model from '../sub-components/Model.vue'
export default {
    name:"Featuredproducts",
    components:{
        Model

   
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .ms_products-target{
        display: inline-block;
        padding: 10px 45px;
        border: 1px solid lightgrey;

    }
</style>