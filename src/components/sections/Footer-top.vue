<template>
    <div class="ms_footer-top">
        <div class="ms_footer-logos text-center">
            <div class="ms_container">
                <h5 class="my-4">BRAND LOGOS</h5>
                <div class="d-flex justify-content-between">
                    <img v-for="(element, index) in arrayLoghi" :key="index" :src="element.src" alt="">
                </div>           
            </div>
        </div>
        <div class="ms_newsletter">
            <div class="ms_container d-flex justify-content-between align-items-center">
                <div class="pb-3">
                    <i class="fa-regular fa-envelope"></i>
                    <h2 class="d-inline-block mx-3">Subscribe now and get special offers</h2>
                </div>
                <div>
                    <input type="text" placeholder="Insert your email">
                    <button class="rounded-pill" type="submit">SEND</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"Footer",
    data(){
        return{
            arrayLoghi:[
                {
                    src: require("../../assets/img/b_logotype_1.png"),
                },
                {
                    src: require("../../assets/img/b_logotype_2.png"),
                },
                {
                    src: require("../../assets/img/b_logotype_3.png"),
                },
                {
                    src: require("../../assets/img/b_logotype_4.png"),
                },
                {
                    src: require("../../assets/img/b_logotype_5.png"),
                },
            ],
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_footer-logos{
        padding: 50px 0;
        background-color: $bottonebiancoavada;
    }
    .ms_newsletter{
        background-color: $grigioscuroavada;
        padding: 130px 0;
        color: white;
        svg{
            color: $grigioavada;
            background-color: $neroavada;
            font-size: 2.2rem;
            padding: 15px;
            border-radius: 50%;
        }
    }
    h5{
        color: #8f8f8f;
    }
    button{
    margin-left: 25px;
    color: white;
    background-color: $bluavada;
    border: none;
    padding: 7px 40px;
    }   
    input{
        border: 0;
        border-radius: 25px;
        padding: 7px;  
        width: 350px;      
    }
</style>