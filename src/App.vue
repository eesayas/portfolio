<template>
  <div id="app">
    <NavBar/>
    <Home msg="Welcome to Your Vue.js App"/>
    <br><br><br>
    <Skills/>
    <br><br><br>
    <Projects/>
  </div>
</template>

<script>
import Home from './components/Home.vue';
import NavBar from "./components/NavBar.vue";
import Skills from "./components/Skills.vue";
import Projects from "./components/Projects.vue";

export default {
  name: 'App',
  components: {
    NavBar,
    Home,
    Skills,
    Projects
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

  #app{
    background-color: #171B1B !important;
    margin: 0 !important;
    padding: 0 !important;
    height: 100%;
    color: #EEDFBB !important;
    font-family: Rubik;
  }
</style>
