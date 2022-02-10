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
            <button type="submit"><b>VIEW ALL</b></button>
            <button type="submit"><b>LOOKBOOK</b></button>
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
        button{
            border: 2px solid white;
            margin: 35px 10px;
            padding: 15px 50px;
            background: rgba(255,255,255, 0.2);
            color: white;
            border-radius: 30px;
            transition: all 300ms ease-in-out;

            &:hover{
                background: rgba(255,255,255, 0);
            }
        }
    }

}
</style>