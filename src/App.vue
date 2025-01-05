<template>
  <div class="d-flex mx-auto">
    <div class="d-flex flex-column px-5" style="width: 40%">
      <About />
    </div>

    <div
      class="ml-5 vh-100 overflow-auto pt-5 flex-1 flex-grow-1 px-5"
      id="projects"
    >
      <Project
        v-for="(project, index) of projects"
        :key="index"
        v-bind="project"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import About from "./components/About.vue";
import Project, { type Props as ProjectProps } from "./components/Project.vue";

const projects: ProjectProps[] = [
  {
    stack: [
      "vue",
      "pinia",
      "tailwind",
      "vuetify",
      "docker",
      "mongodb",
      "nestjs",
      "turborepo",
    ],
    name: "Classie",
    description: "A classroom management software currently in use at a KUMON center in Edmonton.",
    code: "",
    app: "https://www.youtube.com/watch?v=C9_weFglsAU",
  },
  {
    stack: ["webrtc", "preactjs", "deno"],
    name: "Confer",
    description: "A simple video conferencing app.",
    code: "https://github.com/eesayas/iseeya",
    app: "https://iseeya.eesayas.com/",
  },
  {
    stack: ["python", "tensorflow"],
    name: "Object Detection Shell",
    description: "A shell made with Python for training and testing Tensorflow models",
    code: "https://github.com/eesayas/tensorflow-object-detection-shell",
  },
  {
    stack: ["svelte"],
    name: "Isaias & Chalsea",
    description: "A journal web app where you can say your thoughts and have it in writing.",
    code: "https://github.com/eesayas/dear-diary",
    app: "https://dear-diary.online/",
  },
  {
    stack: ["nestjs", "nuxt"],
    name: "PhilSA",
    description: "A corporate website created for the Philippine Students' Association at the University of Alberta",
    app: "https://philsa.ca/",
  },
  {
    stack: ["react"],
    name: "Dear Diary",
    description: "A journal web app where you can say your thoughts and have it in writing.",
    code: "https://github.com/eesayas/dear-diary",
    app: "https://dear-diary.online/",
  },
  {
    stack: ["expressjs", 'bootstrap'],
    name: "reformationedmonton.ca",
    description: "A website for a local church with auto notifications via gmail and webhooks.",
    code: "https://github.com/eesayas/reformationedmonton.ca",
    app: "https://www.reformationedmonton.ca/",
  },

  {
    stack: ["expressjs", "tailwind"],
    name: "hopebargainshoppe.online",
    description: "A booking website for customers of Hope Bargain Shoppe.",
    code: "https://github.com/eesayas/hopebargain",
    app: "https://hopebargainshoppe.online/",
  },

  {
    stack: ["react"],
    name: "Gomoku Online",
    description: "A web game app for Gomoku, an abstract strategy board game. (Worked with a group of 3)",
    code: "https://github.com/ChrisChrisLoLo/GomokuOnline",
    app: "https://chrischrislolo.github.io/GomokuOnline/",
  },
];
</script>

<style scoped>
/* Hide scrollbar for Chrome, Safari and Opera */
#projects::-webkit-scrollbar {
  display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
#projects {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}
</style>
