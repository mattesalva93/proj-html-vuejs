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
                :vocenav=element 
                />
                <div>
                    <button class="rounded-pill" type="submit">SHOP NOW!</button>
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
            vociNav: [
            {
                text: "Home",
                current: true,
            },
            {
                text: "Shop",
                current: false,
            },
            {
                text: "Products",
                current: false,
            },
            {
                text: "Categories",
                current: false,
            },
            {
                text: "News",
                current: false,
            },
            {
                text: "Elements",
                current: false,
            },
        ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

.ms_borders{
    border-bottom: 1px solid #f2f3f3;
    border-top: 3px solid $bluavada;
}
.ms_nav-active{
    color: $bluavada;
    border-top: 3px solid $bluavada;
}
button{
    margin-right: 50px;
    color: white;
    background-color: $bluavada;
    border: none;
    padding: 7px 25px;
}
</style>