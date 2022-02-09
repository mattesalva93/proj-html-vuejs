<template>
    <div class="ms_footer-top">
        <div class="ms_footer-logos text-center">
            <div class="ms_container">
                <h5>Brand Logos</h5>
                <img src="../../assets/img/b_logotype_1.png" alt="">           
                <img src="../../assets/img/b_logotype_1.png" alt="">
                <img src="../../assets/img/b_logotype_1.png" alt="">
                <img src="../../assets/img/b_logotype_1.png" alt="">
                <img src="../../assets/img/b_logotype_1.png" alt="">
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
    name:"Footer"
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