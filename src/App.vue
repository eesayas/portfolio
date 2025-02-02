<template>
  <div class="flex mx-auto flex-col md:flex-row md:h-screen">
    <div class="flex flex-col py-5 md:px-8 md:pt-0 md:w-2/5 overflow-y-auto">
      <About />
    </div>

    <div
      class="md:h-100 overflow-y-auto md:pt-5 flex-1 flex-grow md:px-5 px-3"
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
    description:
      "A classroom management software currently in use at a KUMON center in Edmonton.",
    code: "",
    app: "https://www.canva.com/design/DAFlBNP26RU/mm_OIS_Txjl1uHTF3KKDTA/view?utm_content=DAFlBNP26RU&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h0dabcdee3c",
  },
  {
    stack: ["webrtc", "preactjs", "deno"],
    name: "Confer",
    description: "A simple peer-to-peer video conferencing app.",
    code: "https://github.com/eesayas/confer",
    app: "https://confer.isaiasbriones.com/",
  },
  {
    stack: ["python", "tensorflow"],
    name: "Object Detection Shell",
    description:
      "A Python shell for training and testing machine learning models, featuring real-time object detection in live video streams.",
    code: "https://github.com/eesayas/tensorflow-object-detection-shell",
  },
  {
    stack: ["nestjs", "nuxt"],
    name: "PhilSA",
    description:
      "A corporate website created for the Philippine Students' Association at the University of Alberta during the 2021-2022 academic year.",
    code: "https://github.com/eesayas/philsa.ca",
  },
  {
    stack: ["react"],
    name: "Dear Diary",
    description:
      "A journal web app where you can say your thoughts and have it in writing. (Worked with a group of 2)",
    code: "https://github.com/eesayas/dear-diary",
    app: "https://diary.isaiasbriones.com/",
  },
  {
    stack: ["expressjs", "bootstrap"],
    name: "reformationedmonton",
    description:
      "A website for a local church in Edmonton, Alberta, which was active from 2017 to 2024.",
    code: "https://github.com/eesayas/reformationedmonton.ca",
  },

  {
    stack: ["expressjs", "tailwind"],
    name: "hopebargainshoppe",
    description:
      "A booking website for Hope Bargain Shoppe to manage customer visits and store capacity during the COVID-19 pandemic.",
    code: "https://github.com/eesayas/hopebargain",
  },

  {
    stack: ["react"],
    name: "Gomoku Online",
    description:
      "A web game app for Gomoku, an abstract strategy board game. (Worked with a group of 3)",
    code: "https://github.com/ChrisChrisLoLo/GomokuOnline",
    app: "https://chrischrislolo.github.io/GomokuOnline/",
  },
];
</script>
