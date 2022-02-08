<template>
<div class="nav-element">
    {{vocenav}}
    <i class="fas fa-chevron-down"></i> 
</div>
</template>

<script>

export default {
    name:"Nav",
    props:{
        'vocenav': String,
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/globals.scss';

    .nav-element{
        line-height: 80px;
        vertical-align: middle;
    }


</style>