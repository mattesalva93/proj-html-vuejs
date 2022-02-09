<template>

<div class="ms_collection-container">
    <div v-for="(element, index) in collezioniArray" 
        :key="index" 
        class="ms_collection-box">
        <img 
        :src="element.src"
        :alt="element.nome">
        <div class="ms_collection-text">
            <h5>{{element.nome}}</h5>
            <h6>{{element.subnome}}</h6>
            <button class="btn btn-primary rounded-pill" type="submit">View More</button>
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
            .ms_collection-text{
                position: absolute;
                bottom: 20%;
                left: 50%;
                transform: translate(-50%);
            }
        }
    }



</style>