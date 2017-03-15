
<template>

    <ul class="aside-ul">
        <li class="aside-li" v-for="item in items">
            <a class="aside-a" :href="item.url" target="_blank">{{item.name}}</a>
        </li>
    </ul>

</template>

<script>
    import asideJson from '../lib/aside-ul.json';

    export default {
        data () {
            return {
                items: asideJson.items
            }
        }
    }
</script>

<style>

    .aside-li{
        margin-bottom: 10px;
        border-radius: 10px 0 0 10px;
        background: #00bfa5;
        box-shadow: 0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12);
        list-style: none;
    }
    .aside-a{
        display: inline-block;
        width: 80px;
        height: 38px;
        line-height: 38px;
        padding-left: 10px;
        color: #fff;
        text-decoration: none;
    }

    .aside-a:hover{
        color: #b3f7f9;
    }

</style>