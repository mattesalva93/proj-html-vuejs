<template>
  <div class="ms_container d-flex">
    <div class="ms_container-products">
      <h4>Featured</h4>
      <Products-list-category 
      v-for="(element, index) in modelliFeatured" 
      :key="index"
      :prodotto="element"/>  
    </div>
    <div class="ms_container-products">
      <h4>On Sale</h4>
      <Products-list-category 
      v-for="(element, index) in modelliOnSale" 
      :key="index"
      :prodotto="element"/>  
    </div>
    <div class="ms_container-products">
      <h4>Top rated</h4>
      <Products-list-category 
      v-for="(element, index) in modelliTopRated" 
      :key="index"
      :prodotto="element"/>  
    </div>
    <div class="ms_container-products">
      <h4>Latest Review</h4>
      <div class="ms_single-product"
      v-for="(element, index) in reviews" :key="index">
        <div class="ms_single-product-text">
        <div>
          {{element.title}}
        </div>
        <div>
          <span v-for="stars in element.stelline" :key="stars"><i class="fas fa-star"></i></span>
        </div>
        <div> 
          by {{element.author}}
        </div>
      </div>
      <div class="ms_single-product-img">
        <img :src="element.src" alt="">
      </div>
    </div>
    </div>
  </div>      
</template>

<script>
import ProductsListCategory from '../sub-components/Products-list-category.vue'
import products from '../data/avada.js';

export default {
  components: {
    ProductsListCategory 
    },
    name:"Productslist",
    data(){
      return{
        modelli: products,
        modelliTopRated: [],
        modelliOnSale: [],
        modelliFeatured: [],
        reviews: [
          {
            title: "Black Leather Jacket",
            stelline: 5,
            author: "admin",
            src: require("../../assets/img/black_elegant_leather_jacket-200x260.jpg")
          },
          {
            title: "Leather Gloves",
            stelline: 5,
            author: "beardman",
            src: require("../../assets/img/leather_gloves-200x260.jpg")
          },
          {
            title: "Spring Printed Dress",
            stelline: 5,
            author: "admin",
            src: require("../../assets/img/spring_printed_dress-200x260.jpg")
          },
        ]
      }
    },
    created(){
      this.getFeatured();
      this.getToprated();
      this.getOnSale();
    },
    methods:{
      getFeatured(){
        this.modelliFeaturedAll = this.modelli.filter(element => element.featured);
        this.modelliFeatured = this.modelliFeaturedAll.filter(element => element.inevidenza);
      },
      getToprated(){
        this.modelliTopRated = this.modelli.filter(element => element.toprated);
      },
      getOnSale(){
        this.modelliOnSale = this.modelli.filter(element => element.onsale);
      }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .ms_container-products{
        width: 22%;
        margin: 0 auto;
    }
    .ms_container-products:first-child{
        margin-left: 0;
    }
    .ms_container-products:last-child{
        margin-right: 0;
    }
    .ms_single-product{
            display: flex;
            height: 100px;
            border-bottom: 1px solid lightgray;
            padding: 10px 0;
            .ms_single-product-text{
                width: 75%;
            }
            .ms_single-product-img{
                width: 25%;
                img{
                    height: 100%;
                    width: 100%;
                }
            }
        }

</style>