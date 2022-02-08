<template>
<div class="container">
    <div class="row">
        <Headertop />
    </div>
    <div class="row">
        <div class="col d-flex justify-content-between align-items-center">
            <div>
                <img src="../../assets/img/classic_shop_logo1x.png" alt="">
            </div>
            <div class="d-flex align-items-center">
                <Nav 
                v-for="(element, index) in elementiNav" 
                :key="index" 
                :vocenav=element />

                <div>
                    <button class="btn btn-primary rounded-pill" type="submit">SHOP NOW!</button>
                    <i class="fas fa-search"></i>
                </div>
            </div>
        </div>
    </div>
    <div class="row">
        <div class="col-12 text-center">
            Jumbotron 
        </div>
    </div>
</div>
</template>

<script>
import Headertop from '../sections/Header-top.vue'
import Nav from '../sections/Nav.vue'
export default {
    name:"Header",
    components: {
        Headertop,
        Nav
    },
    data(){
        return{
            elementiNav: ['Home', 'Shop', 'Products', 'Categories', 'News', 'Elements']
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
</style>