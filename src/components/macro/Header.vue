<template>
    <header>
        <div class="ms_borders">
        <Headertop />
        </div>
        <div class="d-flex justify-content-between align-items-center ms_container">
            <div>
                <img src="../../assets/img/classic_shop_logo1x.png" alt="">
            </div>
            <div class="d-flex align-items-center">
                <Nav 
                v-for="(element, index) in vociNav" 
                :key="index" 
                :vocenav=element />
                <div>
                    <button class="btn btn-primary rounded-pill" type="submit">SHOP NOW!</button>
                    <i class="fas fa-search"></i>
                </div>
            </div>
        </div>
        <Jumbotron /> 
    </header>
</template>

<script>
import Headertop from '../sections/Header-top.vue'
import Jumbotron from '../sections/Jumbotron.vue'
import Nav from '../sections/Nav.vue'

export default {
    name:"Header",
    components: {
        Headertop,
        Nav,
        Jumbotron
    },
    data(){
        return{
            vociNav: ['Home', 'Shop', 'Products', 'Categories', 'News', 'Elements']
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

.ms_borders{
    border-bottom: 1px solid lightgrey;
    border-top: 2px solid blue;
}
</style>