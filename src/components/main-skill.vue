
<template>
    <div class="main-skill">
        <dt><i class="icon iconfont iconfontMax icon-tag"></i>Skill. 技能清单</dt>
        <ul class="SkillUl">
            <li class="SkillLi" v-for="skill in skills">
                <h3>{{skill.name}}</h3>
                <ul class="SkillDataUl">
                    <li class="SkillData" v-for="data in skill.datas">
                        <div class="circle"></div>
                        <h4>{{data.title}}</h4>
                        <p>{{data.text}}</p>
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</template>

<script>

    import mainSkill from '../lib/main-skill.json';
    export default {
        data () {
            return {
                skills: mainSkill.skills,
            }
        }
    }

</script>

<style>

    .main-skill{
        position: relative;
        width: 100%;
    }

    .main-skill dt{
        font-size: 26px;
        color: #00796b;
        line-height: 30px;
        border-bottom: 1px solid #00796b;
        margin: 0 0 15px -5px
    }

    .main-skill h3{
        color: #004d40;
        margin: 0 0 30px 5px;
        font-size: 20px;
    }

    .main-skill ul{
        list-style: none;
    }

    .SkillDataUl{
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

    .SkillDataUl h4{
        position: relative;
        top: -12px;
        line-height: 30px;
        font-size: 18px;
        bottom: 3px;
        color: #000;
    }

    .SkillDataUl p{
        position: relative;
        top: -6px;
        font-size: 15px;
        line-height: 22px;
        margin-left: 15px;
        margin-bottom: 8px;
        color: #616161;
    }

</style>