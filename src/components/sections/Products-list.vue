<template>
<div class="ms_container d-flex">
    <products-list-category />    
    <products-list-category />
    <products-list-category />
    <products-list-category />
</div>
</template>

<script>
import ProductsListCategory from '../sub-components/Products-list-category.vue'

export default {
  components: { ProductsListCategory },
    name:"Productslist",

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';


</style>