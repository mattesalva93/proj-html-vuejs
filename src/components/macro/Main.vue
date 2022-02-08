<template>
<div>

    <Featuredproducts />

    <Collection />

    <Bestseller />

    <div class="row">
        <div class="col-12 text-center">
            sezione componente "sconti" x2
        </div>
    </div>
    <div class="row">
        <div class="col-12 text-center">
            sezione con componente "modello"x5 voce new arrivals
        </div>
    </div>
    <div class="row">
        <div class="col-12 text-center">
            sezione con componente "citazioni"
        </div>
    </div>
    <div class="row">
        <div class="col-12 text-center">
            sezione con componente "voce-blog"x3 from our blog
        </div>
    </div>
    <div class="row">
        <div class="col-12 text-center">
            sezione con componente "lista prodotti" voce best seller
        </div>
    </div>
</div>
</template>

<script>

import Featuredproducts from '../sections/Featured-Products.vue'
import Collection from '../sections/Collection.vue'
import Bestseller from '../sections/Bestseller.vue'

export default {
  components: { 
    Featuredproducts,
    Collection,
    Bestseller,
    
    },
    name:"Main"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

</style>