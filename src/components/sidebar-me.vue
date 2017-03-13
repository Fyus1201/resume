
<template>

    <div class="sidebar-me">
        <dt><i class="icon iconfont iconfontMed icon-tag"></i>About me. 个人介绍</dt>
        <ul>
            <li class="about-li " v-for="aboutme in about">
                <p>{{aboutme}}</p>
            </li>
        </ul>


        <div class="sidebar-resume">
            <dt><i class="icon iconfont iconfontMed icon-tag"></i>Resume. 在线简历</dt>
            <div>
                <img :src="imgUrl">
                <br>
                <a :href="url" target="_blank">{{url}}</a>
            </div>
        </div>
    </div>

</template>

<script>

    import sidebarMe from '../lib/sidebar-me.json';
    console.log(sidebarMe.about);
    export default {
        data () {
            return {
                about: sidebarMe.about,
                imgUrl: sidebarMe.img,
                url: sidebarMe.url,
            }
        }
    }


</script>

<style>

    .sidebar-me{
        margin: 35px 0 20px;
    }

    .sidebar-me dt{
        font-size: 18px;
        color: #9f3;
        line-height: 40px
    }

    .sidebar-me p{
        text-indent: 2em;
        color: #004d40;
        font-size: 18px;
    }

    .sidebar-resume{
        position: relative;
        color: #004d40;
        display: none;
    }
    .sidebar-resume div{
        text-align: center;
    }
    .sidebar-me img{
        width: 200px
    }

    .sidebar-me div a{
        color: #004d40;
        text-decoration: none;
    }

    .about-li{
        list-style: none;
    }

</style>