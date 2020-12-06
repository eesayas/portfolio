<template>
<div id="app" class="d-flex h-100">
  <div class="d-flex mx-auto">
    <div class="d-table" style="padding-top: 6.5vw" id='left-panel'>
      <About/><br>
      <Skills/><br><br>
      <Contact/>
    </div>
    
    <div class="ml-5 h-100" id="projects">
      <Project v-for="p in projects" :key="p.name" :data="{p}"/>
    </div>
  </div>
</div>
</template>

<script>

import About from "./components/About.vue"
import Skills from "./components/Skills.vue"
import Contact from "./components/Contact.vue"
import Project from "./components/Project.vue"


export default {
  name: 'App',
  components: {
    About, Skills, Contact, Project
  },
  data(){
    return {
      projects: [
        {
          langs: ['webrtc', 'peerjs'],
          name: 'iSeeYa',
          desc: 'A simple video conferencing app that uses PeerJS and WebRTC.',
          code: 'https://github.com/eesayas/iseeya',
          app: "https://iseeya.eesayas.com/",
        },
        { 
          langs: ['reactjs', 'javascript', 'mongodb'],
          name: 'Classie',
          desc: 'A ReactJS web application for student and staff management of a teaching centre.',
          code: 'https://github.com/eesayas/classie.ca',
          app: "https://www.youtube.com/watch?v=C9_weFglsAU",
        },

        {
          langs: ['python', 'django', 'webscrapping'],
          name: 'Gander',
          desc: 'A Django web app for deciding what Netflix movie to watch with only a limited time.',
          code: 'https://github.com/eesayas/Gander',
          app: "https://gander-netflix.herokuapp.com/",
        },

        {
          langs: ['wit.ai', 'speech recognition', 'speech-to-text'],
          name: 'Dear Diary',
          desc: 'A journal web app where you can say your thoughts and have it in writing.',
          code: 'https://github.com/eesayas/dear-diary',
          app: "https://dear-diary.online/",
        },

        {
          langs: ['java', 'android', 'firebase'],
          name: 'Mooood',
          desc: 'An Android social media, mobile app for sharing your moods.',
          code: 'https://github.com/eesayas/Mooood',
          app: "https://www.youtube.com/watch?v=ONhTewFSVVo",
        },

        {
          langs: ['chrome extension', 'javascript'],
          name: 'Watch Your Profanity',
          desc: 'A google chrome extension for filtering f-words from Netflix.',
          code: 'https://github.com/eesayas/watch-your-profanity',
          app: "https://www.youtube.com/watch?v=ONhTewFSVVo",
        },


        {
          langs: ['expressjs', 'googleapis', 'webhooks'],
          name: 'reformationedmonton.ca',
          desc: 'A website for a local church with auto notifications via gmail and webhooks.',
          code: 'https://github.com/eesayas/reformationedmonton.ca',
          app: "https://www.reformationedmonton.ca/",
        },

        {
          langs: ['tailwindcss', 'expressjs'],
          name: 'hopebargainshoppe.online',
          desc: 'A booking website for customers of Hope Bargain Shoppe.',
          code: 'https://github.com/eesayas/hopebargain',
          app: "https://hopebargainshoppe.online/",
        },
      ]
    }
  }
}
</script>

<style>
@font-face {
  font-family: "Rubik";
  src: url("./fonts/Rubik-Regular.ttf") format("truetype");
}

@font-face {
  font-family: "RubikMedium";
  src: url("./fonts/Rubik-Medium.ttf");
}

@font-face{
  font-family: "RubikLight";
  src: url("./fonts/Rubik-Light.ttf")
}

#projects{
  padding-top: 6vw; 
  overflow-y: scroll;
}

/* Hide scrollbar for Chrome, Safari and Opera */
#projects::-webkit-scrollbar {
    display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
#projects {
  -ms-overflow-style: none;  /* IE and Edge */
  scrollbar-width: none;  /* Firefox */
}

@media screen and (max-width: 1250px) {
  #projects{
    margin-left: 1rem !important;
  }

  #app{
    padding: 0 2rem;
  }
}

@media screen and (max-width: 845px) {
  #left-panel{
    background-color: #151515;
    width: 100%;
  }

  #projects{
    margin-left: 0 !important;
  }

  #app{
    height: auto !important;
  }

  #app > div{
    flex-direction: column;
  }
}
</style>
