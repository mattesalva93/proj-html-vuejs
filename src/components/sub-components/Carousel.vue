<template>

    <div class="ms_model-carousel-container">
        <div class="ms_carousel-buttons rx">
            <i class="fas fa-chevron-right"></i>
        </div>
        <img :src="modello.src" alt=""/>
        <div class="ms_carousel-buttons lx">
            <i class="fas fa-angle-left"></i>
        </div>
    </div>

</template>


<script>
export default {
    name:"Carousel",
    props: {
        'modello': Object,
    }
    
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_model-carousel-container{
        position: relative;
        img{
            width: 20%;
        }
        .ms_carousel-buttons{
            position: absolute;
            top: 50%;
            padding: 10px 6px;
            background-color: lightgrey;
            color: white;
            font-size: 0.8rem;
        }
        .lx{
            left: 1%;
        }
        .rx{
            right: 1%;
        }
    }
</style>