<template>
    <div class="ms_container-products">
        <h4>Featured</h4>
        <div class="ms_single-product">
            <div class="ms_single-product-text">
                <span>Black Jacket $125</span> <br>
                <span>stelline</span> <br>
                <span>eventuale sconto </span>
            </div>
            <div class="ms_single-product-img">
                <img src="../../assets/img/black_leather_jacket-120x156.jpg" alt="">
            </div>
        </div>
        <div class="ms_single-product">
            <div class="ms_single-product-text">
                <span>Black Jacket $125</span> <br>
                <span>stelline</span> <br>
                <span>eventuale sconto </span>
            </div>
            <div class="ms_single-product-img">
                <img src="../../assets/img/black_leather_jacket-120x156.jpg" alt="">
            </div>
        </div>
        <div class="ms_single-product">
            <div class="ms_single-product-text">
                <span>Black Jacket $125</span> <br>
                <span>stelline</span> <br>
                <span>eventuale sconto </span>
            </div>
            <div class="ms_single-product-img">
                <img src="../../assets/img/black_leather_jacket-120x156.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name:"Productslistcategory",

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .ms_container-products{
        width: 22%;
        margin: 0 auto;
        .ms_single-product{
            display: flex;
            height: 100px;
            border-bottom: 1px solid lightgray;
            padding: 10px 0;
            .ms_single-product-text{
                width: 75%;
            }
            .ms_single-product-img{
                width: 25%;
                img{
                    height: 100%;
                    width: 100%;
                }
            }
        }
    }
    .ms_container-products:first-child{
        margin-left: 0;
    }
    .ms_container-products:last-child{
        margin-right: 0;
    }



</style>