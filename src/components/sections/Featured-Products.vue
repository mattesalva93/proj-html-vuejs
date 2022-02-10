<template>
<div class="ms_container ms_margin">
    <h2>Featured Products </h2>
    <h6>Must have products from our top sellers</h6>
    <div class="ms_products-target" 
    @click="elencoAttivo = 'men'"
    :class="{'ms_products-target-active': elencoAttivo == 'men'}">
        Men
    </div>
    <div class="ms_products-target" 
    @click="elencoAttivo = 'women'"
    :class="{'ms_products-target-active': elencoAttivo == 'women'}">
        Women
    </div>
    <div class="ms_products-target" 
    @click="elencoAttivo = 'accessories'"
    :class="{'ms_products-target-active': elencoAttivo == 'accessories'}">
        Accessories
    </div>
    <div
    v-if="elencoAttivo == 'men'"  
    class="ms_models-container">
        <Model 
        v-for="(element, index) in modelliUomini" 
        :key="index"
        :capo="element" />
    </div>
    <div
    v-if="elencoAttivo == 'women'"  
    class="ms_models-container">
        <Model 
        v-for="(element, index) in modelliDonne" 
        :key="index"
        :capo="element" />
    </div>
    <div
    v-if="elencoAttivo == 'accessories'"  
    class="ms_models-container">
        <Model 
        v-for="(element, index) in modelliAccessori" 
        :key="index"
        :capo="element" />
    </div>
    
</div>
</template>

<script>
import Model from '../sub-components/Model.vue'
import products from '../data/avada.js';

export default {
    name:"Featuredproducts",
    components:{
        Model
    },
    data(){
        return{
            modelli: products,
            modelliUomini: [],
            modelliDonne: [],
            modelliAccessori: [],
            elencoAttivo: "men"
        }
    },
    created (){
        this.getAccessori();
        this.getModelliUomini();
        this.getModelliDonne();

    },
    methods: {
        getModelliUomini (){
            this.modelliFeatured = this.modelli.filter(element => element.featured);
            this.modelliUomini = this.modelliFeatured.filter(element => element.target == 'men');
            console.log(this.modelliUomini)
        },
        getModelliDonne (){
            this.modelliFeatured = this.modelli.filter(element => element.featured);
            this.modelliDonne = this.modelli.filter(element => element.target == "women");
            console.log(this.modelliDonne)
        },
        getAccessori (){
            this.modelliFeatured = this.modelli.filter(element => element.featured);
            this.modelliAccessori = this.modelli.filter(element => element.target == "accessories");
            console.log(this.modelliAccessori)
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .ms_products-target{
        display: inline-block;
        padding: 10px 45px;
        border: 1px solid $bordiavada;
        background-color: #f5f5f5;
        
    }
    .ms_products-target-active{
        background-color: white;
        margin: 50px 0;
    }
    .ms_models-container{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .ms_margin{
        padding: 100px 0;
        text-align: center;
        h6{
            color: $grigioavada;
        }
    }
    
</style>