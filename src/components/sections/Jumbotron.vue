<template>
<div class="ms_jumbotron">
    <div class="ms_jumbotron-text">
        <h1>
            Brand New Arrivals
        </h1>
        <h3 class="mt-3">
            NEW COLLECTION FROM NEW YORK
        </h3>
        <div>
            <button class="btn btn-primary rounded-pill" type="submit">VIEW ALL</button>
            <button class="btn btn-primary rounded-pill" type="submit">LOOKBOOK</button>
        </div>
    </div>
</div>
</template>

<script>

export default {
    name:"Jumbotron",

}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

.ms_jumbotron{
    height: 911px;
    background-image: url(../../assets/img/home1_slide_three_bg_2.jpg);
    background-size: cover;
    background-position: center;
    position: relative;
    color: white;
    .ms_jumbotron-text{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
        h1{
            font-size: 7rem;
        }
    }

}
</style>