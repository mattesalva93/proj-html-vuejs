<template>
    <div class="ms_model-box">
        <div class="ms_model-img">
            <img :src="capo.src" alt="">
            <div class="ms_model-hover">
                <i class="fa-regular fa-square-check"></i>
            </div>
        </div>
            <div class="ms_model-text">
                <h6>{{capo.modello}}</h6>
                <span>{{capo.tipologia}}</span> <br>
                <p v-if="capo.sconto == true">
                    <s>{{capo.prezzo}}</s>
                    {{capo.prezzoscontato}}
                </p>
                <p v-else> {{capo.prezzo}}</p>
            </div>
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

    .ms_model-box{
        width: 25%;
        .ms_model-text{
            text-align: left;
        h6{
            margin: 0;
        }
            
        span:nth-of-type(1){
            color: $grigioavada;
            font-size: 0.9rem;
        }
        p:last-child{
            margin-top: 0.5rem;
            margin-bottom: 0;
            color: $bluavada;
        }
        }
    }
    s{
        font-size: 0.8rem;
    }
    .ms_model-img{
        position: relative;
        .ms_model-hover{
            display: none;
            svg{
                padding: 20px;
                font-size: 2rem;
                border-radius: 50%;
                color: white;
                background-color: $grigioscuroavada;
            }
        }
        &:hover .ms_model-hover{
            position: absolute;
            top:0;
            left: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100%;
            width: 100%;
            background-image: linear-gradient($bluavada, $rosaavada);
            opacity: 0.9;
            cursor: pointer;
        }
    }
    
    
</style>