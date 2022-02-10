<template>
    <div class="ms_article-box">
        <img :src="articolo.src" alt="">
        <h6>{{articolo.title}}</h6>
        <span>{{articolo.date}}</span> <span>| {{articolo.comments}}</span>
        <p>{{articolo.text}}</p>
    </div>
</template>

<script>

export default {
    name:"Ourblog",
    props:{
        'articolo': Object
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
    .ms_article-box{
        width: 31%;
        text-align: left;
        img{
            height: 65%;
            width: 100%;
        }

    }
    .ms_article-box:nth-of-type(2){
        margin: 0 3.5%;
    }

</style>