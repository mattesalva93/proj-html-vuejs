<template>
    <div class="nav-element"
    :class="{'ms_nav-active': vocenav.current}">
        {{vocenav.text}}
        <i class="fas fa-chevron-down"></i> 
    </div>
</template>

<script>

export default {
    name:"Nav",
    props:{
        'vocenav': Object,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .nav-element{
        line-height: 80px;
        vertical-align: middle;
        margin-right: 50px;
        svg{
            font-size: 0.6rem;
            margin-left: 5px;
            padding-bottom: 2px;
        }
    }


</style>