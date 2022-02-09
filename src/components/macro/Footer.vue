<template>
<footer>
    <Footer-top />

    <div class="ms_footer-main">
        <div class="ms_container d-flex">
            <div class="ms_footer-section py-5">
                <img src="../../assets/img/classic_shop_logo1x.png" alt="">
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Expedita ad impedit distinctio ipsam officia ex amet quas inventore. Tempora earum labore at dicta! Dolorum optio necessitatibus a atque assumenda veritatis.</p>
                <div class="social-icons">
                    <i class="fab fa-facebook-f"></i>
                    <i class="fab fa-twitter"></i>            
                    <i class="fab fa-instagram"></i>
                    <i class="fab fa-youtube"></i>
                </div>
            </div>
            <Products-list-category 
            class="py-5"/>
            <div class="ms_footer-section ms_footer-blog-links py-5">
                <h4>recent posts</h4>
                <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
                <p><i class="fas fa-angle-right"></i> Lorem ipsum dolor sit amet</p>
            </div>
            <div class="ms_footer-section py-5">
                <h4>Tags</h4>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>
                <div class="ms_footer-tags">
                    Black
                </div>

            </div>
        </div>
    </div>

    <div class="ms_footer-bottom text-center">
        <span> &#169; Copyright 2012-2020 | Avada Theme by Theme Fusion | All Rights Reseverved | Powered by WordPress</span>
       
    </div>
</footer>
</template>

<script>
import FooterTop from '../sections/Footer-top.vue'
import ProductsListCategory from '../sub-components/Products-list-category.vue'
export default {
    components: {
        FooterTop,
        ProductsListCategory 

    },
    name:"Footer"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .ms_footer-main{
        background-color: lightgreen;
        .ms_footer-section{
            width: 22%;
            height: 85px;
            margin: 0 auto;
        }
        .ms_footer-section:first-child{
            margin-left: 0;
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
                border-bottom: 1px solid lightgrey;
                padding-bottom: 1rem;
            }
        }
        .ms_footer-tags{
            border: 1px solid lightgrey;
            display: inline-block;
            padding: 8px;
            margin-right: 2px;
        }
    }
    .ms_footer-bottom{
        padding-top: 25px;
        color: white;
        background-color: black;
    }
</style>