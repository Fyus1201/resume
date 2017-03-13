
<template>

    <ul class="sidebar-info">
        <li class="sidebar-li sidebar-li_other">
            <dt><i class="icon iconfont iconfontMed icon-tag"></i>Contact. 联系方式</dt>
            <dd> <i class="icon iconfont icon-qq"></i>企鹅：<a :href="chatQQ" target="_blank">{{qq}}</a></dd>
            <dd> <i class="icon iconfont icon-shouji"></i>电话：<span >{{phone}}</span ></dd>
            <dd> <i class="icon iconfont icon-youxiang"></i>邮箱：<a :href="chatMail" target="_blank">{{email}}</a></dd>
        </li>
        <li class="sidebar-li_other">
            <dt><i class="icon iconfont iconfontMed icon-tag"></i>Application. 应聘岗位</dt>
            <ul>
                <li class="sidebarTech-li application-li" v-for="application in applications">
                    <dd>{{application.title}}</dd>
                </li>
            </ul>
        </li>
        <li class="sidebar-li_other">
            <dt><i class="icon iconfont iconfontMed icon-tag"></i>Basic info. 基本信息</dt>
            <dd> 个人信息：<span>{{info}}</span></dd>
            <dd> 教育经历：<span >{{education}}</span></dd>
            <dd> 工作经验：<span >{{work}}</span></dd>
            <dd v-if="github"> GitHub：<a :href="github" target="_blank">{{github}}</a></dd>
        </li>
        <li class="sidebar-li_other">
            <dt><i class="icon iconfont iconfontMed icon-tag"></i>Tech. 技能点</dt>
            <ul class="sidebarTech">
                <li class="sidebarTech-li" v-for="tech in techs">
                    <div class="sidebarTech-name">{{tech.name}}</div>
                    <div class="sidebartech-bar-wrap">
                        <div class="sidebarTech-bar" :style="tech.num"></div>
                    </div>
                </li>
            </ul>
        </li>

    </ul>

</template>

<script>

    import sidebarInfo from '../lib/sidebar-info.json';

    const chatQQ = "http://wpa.qq.com/msgrd?v=3&uin=" + sidebarInfo.qq + "&site=qq&menu=yes";
    const chatMail = "mailto:" + sidebarInfo.email;

    export default {
        data () {
            return {
                email: sidebarInfo.email,
                phone: sidebarInfo.phone,
                qq: sidebarInfo.qq,
                techs: sidebarInfo.techs,
                applications: sidebarInfo.applications,
                info: sidebarInfo.info,
                education: sidebarInfo.education,
                work: sidebarInfo.work,
                github: sidebarInfo.github,
                chatQQ: chatQQ,
                chatMail: chatMail,
            }
        }
    }


</script>

<style>

    .sidebar-info{
        list-style: none
    }
    .sidebar-li{
        padding-top: 20px;
        list-style: none;
    }

    .sidebar-li_other {
        margin-top: 20px;
    }

    .sidebar-info dt{
        font-size: 18px;
        color: #9f3;
        line-height: 40px
    }

    .sidebar-info dd{
        margin-left: 15px;
        font-size: 14px;
        line-height: 20px
    }

    .sidebar-info a{
        color: #fff;
        text-decoration: none;
    }

    .application-li{
        margin-left: 15px;
    }

    .sidebarTech-li{
        list-style: none;
        font-size: 14px;
        line-height: 20px
    }
    .sidebarTech-name{
        position: relative;
        width: 90px;
        font-size: 14px;
        display: inline-block;
        top: -3px;
        left: 10px;
    }
    .sidebartech-bar-wrap{
        height: 17px;
        width: 150px;
        background: #00796b;
        display: inline-block;
        border-radius: 20px
    }
    .sidebarTech-bar{
        height: 17px;
        background: #fff;
        border-radius: 20px 0 0 20px
    }

    /*手机*/
    @media screen and (min-width: 600px) and (max-width: 1059px){
        dd{
            text-align: center;
        }
        .sidebarTech-li{
            text-align: center;
        }
        .sidebarTech-name{
            text-align: center;
        }
        .application-li{
            margin-left: 0px;
        }
    }
    @media screen and (max-width: 599px){
        dd{
            text-align: center;
        }
        .sidebarTech-li{
            text-align: center;
        }
        .sidebarTech-name{
            text-align: center;
        }
        .application-li{
            margin-left: 0px;
        }
    }


</style>