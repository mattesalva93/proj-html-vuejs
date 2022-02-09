<template>
    <div class="ms_container text-center">
        <h1>From our blog</h1>
        <h6> the latest classic shop news</h6>    
        <Blog-article />
          
    </div>
</template>

<script>
import BlogArticle from '../sub-components/Blog-article.vue'

export default {
    components: { 
        BlogArticle 
    },
    name:"Ourblog",

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

</style>