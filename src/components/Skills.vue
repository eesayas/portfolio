<template>
    <div id="skills-cont">
        <VueVisibilityTrigger @scrolledIn="skillsIsVisible"/>
        <p class="text-center">SKILLS</p>
        <div class="d-flex justify-content-around mx-5 flex-wrap">
            <div v-for="skill in skills" :key="skill.name" class="d-table skill-circle">
                <radial-progress-bar :diameter="150" :completed-steps="skill.completedSteps" :total-steps="10" startColor="#EEDFBB" stopColor="#EEDFBB" :animateSpeed="700" class="mx-auto mt-5">
                    <p>{{ skill.completedSteps * 10}}%</p>
                </radial-progress-bar>
                <div class="text-center skill-name">{{skill.name}}</div>
            </div>
        </div>
    </div>
</template>

<script>
import RadialProgressBar from 'vue-radial-progress';
import VueVisibilityTrigger from "vue-visibility-trigger";

export default {
    name: "Skills",
    data(){
        return {
            skills: [
                { name: "Javascript", completedSteps: 0 },
                { name: "Python", completedSteps: 0 },
                { name: "C++", completedSteps: 0 },
                { name: "Java", completedSteps: 0 },
                { name: "Dart", completedSteps: 0 },
                { name: "C", completedSteps: 0 },
            ],
            skillsVisible: false,
        }
    },
    methods: {
        skillsIsVisible (isVisible) {
            this.skillsVisible = isVisible;
            this.skills = this.skills.map(skill => {
                return {
                    name: skill.name,
                    completedSteps: isVisible ? 10 : 0
                }
            });
        }
    },
    components: {
        RadialProgressBar, 
        VueVisibilityTrigger
    }
}
</script>

<style scoped>
    p{
        font-size: 2rem;
    }

    .skill-name{
        font-size: 1.5rem;
    }

    .skill-circle{
        width: calc(100% / 3);
    }
</style>