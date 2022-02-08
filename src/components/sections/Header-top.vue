<template>
    <div class="col d-flex justify-content-between align-items-center border-bottom">
        <div class="social-icons">
            <i class="fab fa-facebook-f"></i>
            <i class="fab fa-twitter"></i>            
            <i class="fab fa-instagram"></i>
            <i class="fab fa-youtube"></i>
        </div>
        <div class="shopping">
            <div class="shopping-option">
                <span>Shopping Cart</span> 
            </div>
            <div class="shopping-option">
                <span>Myaccount</span>
                <i class="fas fa-chevron-down"></i> 
            </div>
            <div class="shopping-option">
                <i class="fas fa-shopping-cart"></i>
                <span>CART</span>
                <i class="fas fa-chevron-down"></i>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:"Headertop"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .social-icons svg{
        margin-right: 20px;
    }
    .social-icons svg:last-child{
        margin-right: 0;
    }
    .shopping{
        height: 50px;
        display: flex;
        align-items: center;
        width: 40%;
        .shopping-option{
            width: 27.5%;
            text-align: center;
            line-height: 50px;
            vertical-align: middle;
            svg{
                font-size: 0.8rem;
            }
            span{
                margin: 0 8px;
            }
        }
        .shopping-option:nth-child(2){
            border-left: 1px solid grey;
            border-right: 1px solid grey;

        }
        .shopping-option:last-child{
            width: 45%;
            height: 100%;
            background-color: lightgray;
        }
    }
</style>