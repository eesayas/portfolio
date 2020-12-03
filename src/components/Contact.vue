<template>
<div style="width:300px;" class="d-flex">
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
</style>