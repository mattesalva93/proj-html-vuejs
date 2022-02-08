<template>
<div class="container-fluid">
    <div class="row">
        <Headertop />
    </div>
    <div class="row">
        <div class="col-12 text-center">
            nav
        </div>
    </div>
    <div class="row">
        <div class="col-12 text-center">
            Jumbotron 
        </div>
    </div>
</div>
</template>

<script>
import Headertop from '../sections/Header-top.vue'
export default {
    name:"Header",
    components: {
        Headertop

    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';
</style>