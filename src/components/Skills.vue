<template>
<div>
<h4>SKILLS</h4>
<br>
<div style="width:300px;" v-for="skill in skills" :key="skill.name">
    <div class="d-flex">
        <span style="color:#989898;">{{skill.name}}</span>
        <span class="ml-auto" v-bind:style="{opacity: percentOpacity}" style="transition: 1s;">{{skill.percent}}%</span>
    </div>
    <div class="line" v-bind:style="{width: lineWidth}"></div>
</div>

</div>
</template>

<script>

export default {
    name: "Skills",
    data(){
        return {
            skills: [
                { name: "Javascript", percent: 100},
                { name: "Python", percent: 100 },
                { name: "C++", percent: 100 },
                { name: "Java", percent: 100 },
                { name: "Dart", percent: 100 },
            ],
            lineWidth: "0px",
            percentOpacity: "0%"
        }
    },
    mounted(){
        setTimeout( ()=> {
            this.lineWidth = "300px";
        }, 500);

        setTimeout( () => {
            this.percentOpacity = "100%";
        }, 1200);
    }
}
</script>

<style scoped>
h4{
    font-family: RubikMedium;
}

.line{
    margin-top: 0.5rem;
    height: 2px;
    background: #fff;
    transition: 1s !important;
}

.percent{
    transition: 1s !important;
    opacity: 0;
}

@keyframes animate {
    0%{
        left: 0;
    }
    50%{
        left: 100%;
    }
}
</style>