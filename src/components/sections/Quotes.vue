<template>
    <div class="ms_quotes-container">
        <div class="ms_quotes-text">
            <img src="../../assets/img/man_testimonial.png" alt="">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nemo reiciendis itaque nostrum veritatis perferendis, soluta totam earum ea temporibus? Ut aliquam aut iusto similique quod odio tempora officia commodi nam?</p>
            <span>Dario Pineda, theme fusion</span>
        </div>
    </div>
</template>

<script>

export default {
    name:"Quotes",

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_quotes-container{
        height: 550px;
        background-image: url(../../assets/img/testimonials_home_1_bg.jpg);
        background-size: cover;
        background-position: center;
        text-align: center;
        color: white;
        position: relative;
        .ms_quotes-text{
            max-width: 40%;
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
    }

</style>