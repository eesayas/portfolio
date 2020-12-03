<template>
<div style="width:300px;" class="d-flex" id="contact-cont">
    <div class="d-flex align-items-center" role="button">
        <font-awesome-icon :icon="['fas', 'file']" size="lg"/>
        <span class="mx-2">Resume</span>
    </div>

    <div class="d-flex align-items-center ml-2" role="button">
        <font-awesome-icon :icon="['fab', 'github']" size="lg"/>
        <span class="mx-2">GitHub</span>
    </div>
    
    <div class="d-flex align-items-center ml-2" role="button">
        <font-awesome-icon :icon="['fab', 'linkedin']" size="lg"/>
        <span class="mx-2">Linkedin</span>
    </div>   
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