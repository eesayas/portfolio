<template>
<div style="width:300px;" class="d-flex" id="contact-cont">
    <a class="d-flex align-items-center" role="button" target="_blank" href="https://www.canva.com/design/DAEDwiJGzjk/LFpSj0awI-DiSK9Q3f0jkw/view?utm_content=DAEDwiJGzjk&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton">
        <font-awesome-icon :icon="['fas', 'file']" size="lg"/>
        <span class="mx-2">Resume</span>
    </a>

    <a class="d-flex align-items-center ml-2" role="button" target="_blank" href="https://github.com/eesayas">
        <font-awesome-icon :icon="['fab', 'github']" size="lg"/>
        <span class="mx-2">GitHub</span>
    </a>
    
    <a class="d-flex align-items-center ml-2" role="button" target="_blank" href="https://www.linkedin.com/in/eesayas/">
        <font-awesome-icon :icon="['fab', 'linkedin']" size="lg"/>
        <span class="mx-2">Linkedin</span>
    </a>   
</div>
</template>

<script>
export default {
    name: "Contact",
    components: {
    }
}
</script>

<style scoped>
span{
    font-family: RubikLight;
    letter-spacing: 0.1rem;
}

a{
    color: white !important;
}

@media screen and (max-width: 845px) {
  #left-panel{
    position: fixed;
    background-color: #151515;
    width: 100%;
    padding-bottom: 2rem;
  }

  #projects{
    margin-left: 0 !important;
  }
}

@media screen and (max-width: 373px) {
    #contact-cont{
        width: 100%;
    }
}
</style>