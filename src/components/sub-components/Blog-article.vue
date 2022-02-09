<template>
    <div class="ms_blog-post-container d-flex">
        <div class="ms_article-box">
            <img src="../../assets/img/post_img_10-320x202.jpg" alt="">
            <h6>Lorem ipsum dolor sit amet</h6>
            <span>September 9 2015</span> <span>| 0 comments</span>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure, corrupti, quaerat eligendi modi</p>
        </div>
        <div class="ms_article-box">
            <img src="../../assets/img/post_img_10-320x202.jpg" alt="">
            <h6>Lorem ipsum dolor sit amet</h6>
            <span>September 9 2015</span> <span>| 0 comments</span>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure, corrupti, quaerat eligendi modi</p>
        </div>
        <div class="ms_article-box">
            <img src="../../assets/img/post_img_10-320x202.jpg" alt="">
            <h6>Lorem ipsum dolor sit amet</h6>
            <span>September 9 2015</span> <span>| 0 comments</span>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure, corrupti, quaerat eligendi modi</p>
        </div>
        
    </div>
</template>

<script>

export default {
    name:"Ourblog",

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