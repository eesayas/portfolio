<template>
    <div role="button">
        <b-card title="classie.ca" img-src="/assets/classie.png" img-alt="Image" img-top tag="article"
            style="max-width: 20rem; color: #171b1b" class="mb-2 mt-4 rounded-0 mx-1">

            <b-card-text>
                A web app for managing student attendance
            </b-card-text>

            <b-button href="#" variant="primary" style="background-color: #eedfbb; color: #171b1b; border: none" v-on:click="toggleDetail">VIEW PROJECT</b-button>
        </b-card>
        <ProjectDetail v-bind:show="show" @toggle="toggleDetail"/>
    </div>
</template>

<script>
import ProjectDetail from "./ProjectDetail.vue";

export default {
    name: "ProjectCard",
    components: {
        ProjectDetail
    },
    data(){
        return {
            show: true
        }
    },
    methods: {
        toggleDetail() {
            this.show = !this.show;
        }
    }
}
</script>

<style scoped>

</style>
