<template>
<footer>
    <Footer-top />

    <div class="ms_footer-main">
        <div class="ms_container d-flex">
            <div class="ms_footer-section py-5 d-flex flex-column justify-content-between">
                <img src="../../assets/img/classic_shop_logo_footer.png" alt="">
                <div>
                    <p>Lorem ipsum dolor sit</p>
                    <p>Lorem ipsum dolor sit</p>
                    <p>Lorem ipsum dolor sit</p>
                    <p>Lorem ipsum dolor sit</p>
                    <p>Lorem ipsum dolor sit</p>
                </div>
                <div class="social-icons">
                    <i class="fab fa-facebook-f"></i>
                    <i class="fab fa-twitter"></i>            
                    <i class="fab fa-instagram"></i>
                    <i class="fab fa-youtube"></i>
                </div>
            </div>
            <div class="ms_footer-section d-flex flex-column justify-content-between py-5">
                <h6>TOP RATED PRODUCTS</h6>
                <Products-list-category 
                v-for="(element, index) in modelliTopRated" 
                :key="index"
                :prodotto="element"/>  
            </div>
            <div class="ms_footer-section ms_footer-blog-links py-5 d-flex flex-column justify-content-between">
                <h6>RECENT POSTS</h6>
                <div>
                    <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                    <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                    <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                    <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                    <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                    <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                </div>
            </div>
            <div class="ms_footer-section py-5">
                <h6>TAGS</h6>
                <div v-for="element in arrayTags" :key="element" class="ms_footer-tags">
                    {{element}}
                </div>
            </div>
        </div>
    </div>

    <div class="ms_footer-bottom text-center">
        <span> &#169; Copyright 2012-2020 | Avada Theme by Theme Fusion | All Rights Reseverved | Powered by WordPress</span>
        <div>
            <i class="fa-brands fa-cc-visa"></i>
            <i class="fa-brands fa-cc-paypal"></i>
            <i class="fa-brands fa-cc-mastercard"></i>
            <i class="fa-brands fa-cc-discover"></i>
            <i class="fa-brands fa-cc-amazon-pay"></i>
        </div>
    </div>
</footer>
</template>

<script>
import FooterTop from '../sections/Footer-top.vue'
import ProductsListCategory from '../sub-components/Products-list-category.vue'
import products from '../data/avada.js';

export default {
    name:"Footer",
    components: {
        FooterTop,
        ProductsListCategory 
    },
    data(){
      return{
        modelli: products,
        modelliTopRated: [],
        arrayTags: ['Lorem', 'Ipsum', 'is', 'simply', 'dummy', 'text', 'of', 'the', 'printing', 'and', 'typesetting', 'industry']
      }
    },
    created(){
      this.getToprated();
    },
    methods:{
      getToprated(){
        this.modelliTopRated = this.modelli.filter(element => element.toprated);
      },

    },
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .ms_footer-main{
        background-color: $neroavada;
        color: white;
        .ms_footer-section{
            width: 22%;
            margin: 0 auto;
        }
        .ms_footer-section:first-child{
            margin-left: 0;
            img{
                width: 50%;
            }
            p{
                width: 60%;
                margin: 0;
            }
        }
        .ms_footer-section:last-child{
            margin-right: 0;
        }
        .social-icons svg{
        margin-right: 20px;
        }
        .social-icons svg:last-child{
        margin-right: 0;
        }
        .ms_footer-blog-links{
            p{
                border-bottom: 1px solid $grigioavada;
                padding-bottom: 1rem;
            }
        }
        .ms_footer-tags{
            border: 1px solid $grigioavada;
            display: inline-block;
            padding: 8px;
            margin-right: 2px;
        }
    }
    .ms_footer-bottom{
        padding-top: 25px;
        color: white;
        background-color: #202020;
        svg{
            font-size: 2.5rem;
            margin: 10px;
        }
    }
</style>