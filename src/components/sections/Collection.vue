<template>

<div class="ms_collection-container">
    <div v-for="(element, index) in collezioniArray" 
        :key="index" 
        class="ms_collection-box">
        <img 
        :src="element.src"
        :alt="element.nome">
        <div class="ms_collection-text">
            <h1>{{element.nome}}</h1>
            <h4>{{element.subnome}}</h4>
            <button type="submit"><b>VIEW MORE</b></button>
        </div>
    </div>
</div>

</template>


<script>
export default {
    name:"Collection",
    data(){
        return{
            collezioniArray: [
                {
                    nome: "Winter collection",
                    subnome: "Stylish and warm",
                    src: require("../../assets/img/winter_collection_bg.jpg")
                },
                {
                    nome: "Spring collection",
                    subnome: "Bright and colorful",
                    src: require("../../assets/img/spring_collection_bg.jpg")
                },
                {
                    nome: "Autumn collection",
                    subnome: "Rich and comfortable",
                    src: require("../../assets/img/autumn_collection_bg.jpg")
                },
            ]

        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_collection-container{
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;

        .ms_collection-box{
            width: 33.3333333%;
            height: 900px;
            position: relative;
            text-align: center;
            img{
                height: 100%;
                width: 100%;
            }
            h1{
                font-size: 3rem;
            }
            .ms_collection-text{
                position: absolute;
                bottom: 20%;
                left: 50%;
                transform: translate(-50%);
            }
        }
    }
    button{
        border: 2px solid white;
        margin: 35px 10px;
        padding: 15px 50px;
        background: rgba(255,255,255, 0.2);
        color: white;
        border-radius: 30px;
    }



</style>