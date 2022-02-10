<template>
        <div class="ms_single-product">
            <div class="ms_single-product-text">
                <div>
                    <span>{{prodotto.modello}}</span> 
                    <span v-if="prodotto.stelline == null">
                        <span v-if="prodotto.sconto != true">
                            <b>{{prodotto.prezzo}}</b>
                        </span>
                        <span v-else>
                            <s><b>{{prodotto.prezzo}}</b></s> <br>
                            <span v-if="prodotto.stelline != null">
                                <span v-for="element in prodotto.stelline" :key="element"><i class="fas fa-star"></i></span>
                            </span>
                            <u><b>{{prodotto.prezzoscontato}}</b></u> 
                        </span>
                    </span>
                </div>
                <div v-if="prodotto.stelline != null">
                    <span v-for="element in prodotto.stelline" :key="element"><i class="fas fa-star"></i></span> <br>
                    <span v-if="prodotto.sconto == true"><s><b>{{prodotto.prezzo}}</b></s><u><b>{{prodotto.prezzoscontato}}</b></u></span>
                    <span v-else><b>{{prodotto.prezzo}}</b></span>
                </div>
            </div>
            <div class="ms_single-product-img">
                <img :src="prodotto.src" alt="">
            </div>
        </div>
</template>

<script>

export default {
    name:"Productslistcategory",
    props:{
        'prodotto': Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

        .ms_single-product{
            display: flex;
            height: 100px;
            border-bottom: 1px solid $grigioavada;
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
            svg{
                color: $bluavada;
            }
            
        }
    .ms_container-products:first-child{
        margin-left: 0;
    }
    .ms_container-products:last-child{
        margin-right: 0;
    }
    span{
        color: $grigioavada;
    }
    b, u, s {
        color: #8f8f8f;
    }



</style>