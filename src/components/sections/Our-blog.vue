<template>
<div class="ms_container-our-blog">
    <div class="ms_container text-center">
        <h2>From Our Blog</h2>
        <h6> the latest classic shop news</h6>
        <div class="ms_blog-post-container d-flex">    
            <Blog-article 
            v-for="(element, index) in articoliBlog" 
            :key="index"
            :articolo="element"
            />
        </div>
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

.ms_container-our-blog{
    margin: 100px 0;
    padding-bottom: 50px;
    border-bottom: 1px solid $bordiavada;
    h6{
        padding-bottom: 40px;
        text-transform: capitalize;
        color: $grigioavada;
    }
    h2{
    display: flex;
    justify-content: center;
    align-items: center;
    &:after{
        content: '';
        flex: 1;
        margin-left: 1rem;
        height: 1px;
        background-color: $bordiavada;
    }
    &:before{
        content: '';
        flex: 1;
        margin-right: 1rem;
        height: 1px;
        background-color: $bordiavada;
    }
  }
}
</style>