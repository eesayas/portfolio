<template>
    <div id="projects-cont">
        <p class="text-center">MY PROJECTS</p>
        <div class="d-flex mx-5 my-5 justify-content-around flex-wrap"> 
            <ProjectCard/>
            <!-- <ProjectCard/>
            <ProjectCard/>
            <ProjectCard/> -->
        </div>
    </div>    
</template>

<script>
import ProjectCard from "./ProjectCard.vue";

export default {
    name: "Projects",
    components: {
        ProjectCard
    }
}
</script>

<style scoped>
p{
    font-size: 2rem;
}
</style>