<template>
<div class="ms_promo-container">
    <div class="ms_container">
        <div class="ms_sale-box">
            <div class="ms_sale-text">
                <h1>
                    70% Off
                </h1>
                 <p>
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui exercitationem nisi ea corrupti sapiente?
                </p>
                <button type="submit"><b>VIEW MORE</b></button>
            </div>
        </div>
        <div class="ms_sale-box">
            <div class="ms_sale-text">
                <h1>
                    Free Shipping
                </h1>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui exercitationem nisi ea corrupti sapiente?
                </p>
                <button type="submit"><b>VIEW MORE</b></button>
            </div>
        </div>
    </div>
</div>
</template>

<script>

export default {
    name:"Promo",

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_promo-container{
        height: 520px;
        background-image: url(../../assets/img/bkgd_confetti-compressor.jpg);
        background-size: cover;
        background-position: center;
        color: white;
        .ms_container{
            height: inherit;
            display: flex;
            justify-content: center;
            align-items: center;
            .ms_sale-box{
                height: 75%;
                width: 50%;
                background-image: url(../../assets/img/promo_box_1_bg.jpg);
                background-size: cover;
                background-position: center;
                position: relative;
                .ms_sale-text{
                    position: absolute;
                    top: 30%;
                    left: 10%;
                    p{
                        margin: 1.5rem 0;
                        max-width: 55%;
                    }
                    button{
                        border: 2px solid white;
                        padding: 12px 40px;
                        background: rgba(255,255,255, 0.2);
                        color: white;
                        border-radius: 30px;
                    }
                }
            }
        .ms_sale-box:last-child{
            background-image: url(../../assets/img/promo_box_2_bg.jpg);
            margin-left: 30px;

        }
    }
}

</style>