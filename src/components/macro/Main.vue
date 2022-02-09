<template>
<div>
    <Featuredproducts />

    <Collection />

    <Bestseller />

    <Promo />
    
    <Newarrivals />

    <Quotes />

    <Our-blog />

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
import Promo from '../sections/Promo.vue'
import Newarrivals from '../sections/Newarrivals.vue'
import Quotes from '../sections/Quotes.vue'
import OurBlog from '../sections/Our-blog.vue'

export default {
  components: { 
    Featuredproducts,
    Collection,
    Bestseller,
    Promo,
    Newarrivals,
    Quotes,
    OurBlog,
    
    },
    name:"Main"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

</style>