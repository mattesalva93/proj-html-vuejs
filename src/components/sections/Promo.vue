<template>
<div class="ms_promo-container">
    <div class="ms_container">
        <div class="ms_sale-box">
            <div class="ms_sale-text">
                <h3>
                    70% Off
                </h3>
                 <p>
                     Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui exercitationem nisi ea corrupti sapiente?
                </p>
                <button class="btn btn-primary rounded-pill" type="submit">View More</button>
            </div>
        </div>
        <div class="ms_sale-box">
            <div class="ms_sale-text">
                <h3>
                    Free Shipping
                </h3>
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Qui exercitationem nisi ea corrupti sapiente?
                </p>
                <button class="btn btn-primary rounded-pill" type="submit">View More</button>
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
                    max-width: 60%;
                    top: 30%;
                    left: 10%;
                }
            }
        .ms_sale-box:last-child{
            background-image: url(../../assets/img/promo_box_2_bg.jpg);
            margin-left: 30px;

        }
    }
}

</style>