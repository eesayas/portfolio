<template>
<div id="app" class="d-flex h-100">
  <div class="d-flex mx-auto">
    <div class="d-table" style="padding-top: 6.5vw">
      <About/><br>
      <Skills/><br><br>
      <Contact/>
    </div>
    
    <div class="h-100 ml-5" id="projects">
      <Project/>
      <Project/>
      <Project/>
      <Project/>
      <Project/>
      <Project/>
      <Project/>
      <Project/>
      <Project/>
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
</style>
