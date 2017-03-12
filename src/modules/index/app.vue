
<template>
    <div id="resume">
        <div class="container">
            <div class="sidebar">
                <sidebar-title></sidebar-title>
                <sidebar-info></sidebar-info>
                <sidebar-me></sidebar-me>
            </div>
            <div class="main">

                <!--<main-info></main-info>-->
                <main-experience></main-experience>
                <main-skill></main-skill>

            </div>
        </div>
        <aside>
            <aside-ul></aside-ul>
        </aside>
    </div>
</template>

<script>

    import sidebarTitle from '../../components/sidebar-title.vue'
    import sidebarInfo from '../../components/sidebar-info.vue'
    import sidebarMe from '../../components/sidebar-me.vue'
//
//    import mainInfo from '../../components/main-info.vue'
    import mainExperience from '../../components/main-experience.vue'
    import mainSkill from '../../components/main-skill.vue'

    import asideUl from '../../components/aside-ul.vue'

    export default {
        components: {
            asideUl,
            sidebarTitle,
            sidebarInfo,
            sidebarMe,
//            mainInfo,
            mainExperience,
            mainSkill,
        },
        data () {
            return {

            }

        }
    }
</script>

<style>

    #resume{
        position: relative;
        margin: 0;
        padding: 0;
    }

    @media screen and (min-width: 1060px){
        .container {
            position: relative;
            display: flex;
            margin: 10px auto;
            box-shadow: 0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12);
            width: 1060px;
            overflow: hidden;
            border-radius: 4px;
        }

        .sidebar{
            position: relative;
            box-sizing: border-box;
            width: 300px;
            padding: 15px 20px;
            line-height: 1.5;
            background: #00bfa5;
            color: #fff;
        }
        .main{
            position: relative;
            box-sizing: border-box;
            width: 760px;
            padding: 15px 20px;
            background: #f0f2f1;
        }
        aside{
            position: fixed;
            right: 0;
            top: 30%;
            z-index: 2;
        }

    }

    @media screen and (min-width: 600px) and (max-width: 1059px){
        .container {
            position: relative;
            display: flex;
            margin: 0 auto;
            box-shadow: 0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12);
            width: 100%;
            overflow: hidden;
            border-radius: 4px
        }

        .sidebar{
            position: relative;
            box-sizing: border-box;
            width: 45%;
            padding: 15px 15px;
            line-height: 1.5;
            background: #00bfa5;
            color: #fff;
        }
        .main{
            position: relative;
            box-sizing: border-box;
            width: 55%;
            padding: 20px 20px;
            background: #f0f2f1;
        }
        aside{
            position: fixed;
            right: 0;
            top: 30%;
            z-index: 2;
            display: none;
        }
    }

    @media screen and (max-width: 599px){
        .container {
            position: relative;
            margin: auto;
            box-shadow: 0 2px 2px 0 rgba(0, 0, 0, .14), 0 3px 1px -2px rgba(0, 0, 0, .2), 0 1px 5px 0 rgba(0, 0, 0, .12);
            width: 100%;
            overflow: hidden;
            border-radius: 4px
        }
        .sidebar{
            position: relative;
            box-sizing: border-box;
            width: 100%;
            padding: 30px 30px;
            line-height: 1.5;
            background: #00bfa5;
            color: #fff;
        }
        .main{
            position: relative;
            box-sizing: border-box;
            width: 100%;
            padding: 30px 30px;
            background: #f0f2f1;
        }
        aside{
            position: fixed;
            right: 0;
            top: 30%;
            z-index: 2;
            display: none;
        }
    }


</style>