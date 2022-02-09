<template>
    <div class="ms_container text-center">
        <h1>From our blog</h1>
        <h6> the latest classic shop news</h6>
        <div class="ms_blog-post-container d-flex">    
            <Blog-article 
            v-for="(element, index) in articoliBlog" 
            :key="index"
            :articolo="element"
            />
        </div>
    </div>
</template>

<script>
import BlogArticle from '../sub-components/Blog-article.vue'

export default {
    components: { 
        BlogArticle 
    },
    name:"Ourblog",
    data(){
        return{
            articoliBlog: [
                {
                    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
                    title: 'Lorem Ipsum is simply dummy text',
                    src: require('../../assets/img/post_img_12-320x202.jpg'),
                    date: 'September 9 2015',
                    comments: '0 comments',

                },
                {
                    text: 'Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of',
                    title: 'Contrary to popular belief',
                    src: require('../../assets/img/post_img_11-320x202.jpg'),
                    date: 'September 9 2015',
                    comments: '0 comments',

                },
                {
                    text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry.',
                    title: 'Lorem Ipsum is simply dummy text',
                    src: require('../../assets/img/post_img_10-320x202.jpg'),
                    date: 'September 9 2015',
                    comments: '0 comments',

                }
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

</style>