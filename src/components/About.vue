<template>
<div>
    <h1>My name is <br> Isaias Briones</h1>
    <p>
        I am a Fullstack, Mobile, and Game developer. I am mostly self-taught and I love creating coding projects.
        I am currently in my 4th Year of Specialization in Computing Science with Minor in Business at the University of Alberta.
    </p>  
</div>
</template>

<script>
export default {
    name: "About"
}
</script>

<style scoped>
div{
    width: 500px
}

h1{
    font-family: RubikMedium;
    font-size: 4rem;
    line-height: 0.9;
}
p{
    font-family: RubikLight;
    color: #939393;
    width: 400px;
    font-size: 1.1rem;
}

@media screen and (max-width: 1250px) {
    h1{
        font-size: 3rem;
    }
}

@media screen and (max-width: 562px){
    div{
        width: auto;
    }
}

@media screen and (max-width: 460px){
    p{
        width: auto;
    }
}
</style>