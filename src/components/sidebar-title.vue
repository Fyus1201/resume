<template>

    <div class="sidebar-title">
        <img :src="imgUrl">
        <h1>{{name}}</h1>
        <h3>{{title}}</h3>
    </div>

</template>

<script>

    import sidebarTitle from '../lib/sidebar-title.json';
    export default {
        data () {
             return {
                 imgUrl: sidebarTitle.img,
                 name: sidebarTitle.name,
                 title: sidebarTitle.title,
             }
        }
    }


</script>

<style>

    .sidebar-title{
        margin: 25px 0 20px;
        text-align: center;
    }

    .sidebar-title img{
        display: block;
        margin: 0 auto 15px;
        width: 120px;
        user-select:none;
    }

    .sidebar-title h1{
        font-size: 28px;
        font-weight: 400;
    }
    .sidebar-title h3{
        font-size: 15px
    }

</style>