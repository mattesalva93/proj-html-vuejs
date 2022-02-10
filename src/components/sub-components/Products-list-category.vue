<template>
        <div class="ms_single-product">
            <div class="ms_single-product-text">
                <div>
                    {{prodotto.modello}} 
                    <span v-if="prodotto.stelline == null">
                        <span v-if="prodotto.sconto != true">
                            {{prodotto.prezzo}}
                        </span>
                        <span v-else>
                            <s>{{prodotto.prezzo}}</s> <br>
                            <span v-if="prodotto.stelline != null">
                                <span v-for="element in prodotto.stelline" :key="element"><i class="fas fa-star"></i></span>
                            </span>
                            <u>{{prodotto.prezzoscontato}}</u> 
                        </span>
                    </span>
                </div>
                <div v-if="prodotto.stelline != null">
                    <span v-for="element in prodotto.stelline" :key="element"><i class="fas fa-star"></i></span> <br>
                    <span v-if="prodotto.sconto == true"><s>{{prodotto.prezzo}}</s><u>{{prodotto.prezzoscontato}}</u></span>
                    <span v-else>{{prodotto.prezzo}}</span>
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