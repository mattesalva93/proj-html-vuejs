<template>
    <div class="ms_footer-top">
        <div class="ms_footer-logos text-center">
            <div class="ms_container">
                <h5>Brand Logos</h5>
                <img v-for="(element, index) in arrayLoghi" :key="index" :src="element.src" alt="">           
            </div>
        </div>
        <div class="ms_newsletter">
            <div class="ms_container d-flex justify-content-around">
                <div>
                    <i class="fa-regular fa-envelope"></i>
                </div>
                <div>
                    <h4>Subscribe now and bla bla bla</h4>
                </div>
                <div>
                    <input type="text">
                    <button>Send</button>
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
        background-color: lightgray;
    }
    .ms_newsletter{
        background-color: lightblue;
        padding: 80px 0;
        
    }
</style>