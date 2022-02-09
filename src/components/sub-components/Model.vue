<template>
     <div class="ms_model-box">
        <img :src="capo.src" alt="">
        <h6>{{capo.modello}}</h6>
        <span>{{capo.tipologia}}</span> <br>
        <span v-if="capo.sconto == true">
            <s>{{capo.prezzo}}</s>
            {{capo.prezzoscontato}}
        </span>
        <span v-else> {{capo.prezzo}}</span>
    </div>
</template>


<script>
export default {
    name:"Model",
    props:{
        'capo': Object
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    s{
        font-size: 0.8rem;
    }
    
</style>