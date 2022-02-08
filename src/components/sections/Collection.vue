<template>

<div class="ms_collection-container">
    <div class="ms_collection-box">
        <div class="ms_collection-text">
            <h5>Winter Collection</h5>
            <h6>Stylish and warm</h6>
            <button class="btn btn-primary rounded-pill" type="submit">View More</button>
        </div>
    </div>
    <div class="ms_collection-box">
        <div class="ms_collection-text">
            <h5>Winter Collection</h5>
            <h6>Stylish and warm</h6>
            <button class="btn btn-primary rounded-pill" type="submit">View More</button>
        </div>
    </div>
    <div class="ms_collection-box">
        <div class="ms_collection-text">
            <h5>Winter Collection</h5>
            <h6>Stylish and warm</h6>
            <button class="btn btn-primary rounded-pill" type="submit">View More</button>
        </div>
    </div>
</div>

</template>


<script>
export default {
    name:"Collection"
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
            height: 800px;
            background-image: url(../../assets/img/winter_collection_bg.jpg);
            background-size: cover;
            background-position: center;
            position: relative;
            text-align: center;
            .ms_collection-text{
                position: absolute;
                bottom: 20%;
                left: 50%;
                transform: translate(-50%);
            }
        }
    }



</style>