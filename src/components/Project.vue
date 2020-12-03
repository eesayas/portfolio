<template>
<div id="project" style="padding: 2rem 3rem;" role="button">
    <div class="d-flex">
        <span>REACTJS</span>
        <span>JAVASCRIPT</span>
    </div>
    <h2>Classie</h2>
    <p>A ReactJS web application for student and staff managing of a teaching centre.</p>
</div>
</template>

<script>
export default {
    name: "Project"
}
</script>

<style>
#project{
    background: #202022;
    margin: 1rem 0;
    user-select: none;
}

span{
    margin-left: 0.5rem;
    font-family: RubikLight;
}

span:nth-child(1){
    margin-left: 0;
}

h2{
    font-family: RubikMedium;
}

p{
    color: #939393;
    font-family: RubikLight;
}
</style>