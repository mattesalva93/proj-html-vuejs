<template>
<main>
    <Featuredproducts />

    <Collection />

    <Bestseller />

    <Promo />
    
    <Newarrivals />

    <Quotes />

    <Our-blog />

    <Products-list />
</main>
</template>

<script>

import Featuredproducts from '../sections/Featured-Products.vue'
import Collection from '../sections/Collection.vue'
import Bestseller from '../sections/Bestseller.vue'
import Promo from '../sections/Promo.vue'
import Newarrivals from '../sections/Newarrivals.vue'
import Quotes from '../sections/Quotes.vue'
import OurBlog from '../sections/Our-blog.vue'
import ProductsList from '../sections/Products-list.vue'

export default {
  components: { 
    Featuredproducts,
    Collection,
    Bestseller,
    Promo,
    Newarrivals,
    Quotes,
    OurBlog,
    ProductsList
    
    },
    name:"Main"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

</style>