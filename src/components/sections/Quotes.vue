<template>
    <div class="ms_quotes-container">
        <div class="ms_quotes-text"
        :class="{'ms_quote-active': corrente == 'man'}">
            <img src="../../assets/img/man_testimonial.png" alt="">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nemo reiciendis itaque nostrum veritatis perferendis, soluta totam earum ea temporibus? Ut aliquam aut iusto similique quod odio tempora officia commodi nam?</p>
            <span>Dario Pineda, theme fusion</span>
            <div>
                <span class="ms_full-dot"> </span>
                <span @click="corrente = 'woman'" class="ms_empty-dot"> </span>
            </div>
        </div>
        <div class="ms_quotes-text"
        :class="{'ms_quote-active': corrente == 'woman'}">
            <img src="../../assets/img/woman_testimonial.png" alt="">
            <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nemo reiciendis itaque nostrum veritatis perferendis, soluta totam earum ea temporibus? Ut aliquam aut iusto similique quod odio tempora officia commodi nam?</p>
            <span>Tizia Pineda, theme fusion</span>
            <div>
                <span @click="corrente = 'man'" class="ms_empty-dot"> </span>
                <span class="ms_full-dot"> </span>
            </div>

        </div>
    </div>
</template>

<script>

export default {
    name:"Quotes",
    data(){
        return{
            corrente: "man",
        }
    }

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
            display: none;
            max-width: 40%;
            position: absolute;
            top: 40%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        .ms_quote-active{
            display: inline-block;
        }
        .ms_full-dot:after{
            content: "";
            display: inline-block;
            padding: 7px;
            border-radius: 50%;
            background-color: white;
            margin-right: 5px;
            margin-top: 25px;
        }
        .ms_empty-dot:after{
            content: "";
            display: inline-block;
            padding: 6px;
            border-radius: 50%;
            background-color: transparent;
            border: 1px solid white;
            margin-right: 5px;

        }
    }

</style>