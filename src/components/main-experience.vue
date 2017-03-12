
<template>
    <div class="main-experience">
        <dt><i class="icon iconfont iconfontMax icon-tag"></i>Experience. 项目经验</dt>
        <ul class="ExperienceUl">
            <li class="ExperienceLi" v-for="experience in experiences">
                <h3>{{experience.name}}</h3>
                <ul class="ExperienceDataUl">
                    <li class="ExperienceData" v-for="data in experience.datas">
                        <div class="circle"></div>
                        <h4>{{data.title}}
                            <a v-if="data.github" :href="data.github" target="_blank">
                                <i class="icon iconfont icon-module-link"></i>源码
                            </a>
                            <a v-if="data.demo" :href="data.demo" target="_blank">
                                <i class="icon iconfont icon-module-link"></i>Demo
                            </a>

                        </h4>
                        <p>{{data.text}}</p>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</template>

<script>

    import mainExperience from '../lib/main-experience.json';
    export default {
        data () {
            return {
                experiences: mainExperience.experiences,
            }
        }
    }

</script>

<style>

    .main-experience{
        position: relative;
        width: 100%;
    }

    .main-experience dt{
        font-size: 26px;
        color: #00796b;
        line-height: 30px;
        border-bottom: 1px solid #00796b;
        margin: 0 0 15px -5px
    }

    .main-experience h3{
        color: #004d40;
        margin: 0 0 30px 5px;
        font-size: 20px;
    }

    .main-experience ul{
        list-style: none;
    }

    .ExperienceDataUl{
        position: relative;
        margin: 0 20px 20px 5px;
        padding: 0 0 0 0;
        border-left: 2px solid #00796b;
    }

    .circle{
        height: 14px;
        width: 14px;
        border-radius: 100%;
        background: #00796b;
        float: left;
        position: relative;
        left: -8px;
        top: -5px
    }

    .ExperienceDataUl h4{
        position: relative;
        top: -12px;
        line-height: 30px;
        font-size: 18px;
        bottom: 3px;
        color: #000;
    }

    .ExperienceDataUl p{
        position: relative;
        top: -6px;
        font-size: 15px;
        line-height: 22px;
        margin-left: 15px;
        margin-bottom: 8px;
        color: #616161;
    }

    .ExperienceData a{
        font-size: 13px;
        border: 1px solid #4db6ac;
        color: #4db6ac;
        padding: 1px 3px;
        -webkit-border-radius: 5px;
        border-radius: 5px;
        margin-left: 7px;
        text-decoration: none
    }

</style>