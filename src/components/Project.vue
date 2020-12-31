<template>
<div id="project" style="padding: 2rem 3rem;" role="button">
    <div class="d-flex">
        <span v-for="l in data.p.langs" :key="l" class="langs">{{l}}</span>
    </div>
    <h2>{{data.p.name}}</h2>
    <p>{{data.p.desc}}</p>

    <div class="d-flex">
        <a class="d-flex align-items-center mr-2" role="button" target="_blank" :href="data.p.code" v-if="data.p.code">
            <font-awesome-icon :icon="['fas', 'code']"/>
            <span class="mx-2">Code</span>
        </a>   

        <a class="d-flex align-items-center" role="button" target="_blank" :href="data.p.app" v-if="data.p.app">
            <font-awesome-icon :icon="['fas', 'desktop']"/>
            <span class="mx-2">View App</span>
        </a>  
    </div> 
    
</div>
</template>

<script>
export default {
    name: "Project",
    props: {
        data: Object
    }
}
</script>

<style>
#project{
    background: #202022;
    margin: 1rem 0;
    user-select: none;
    transition: all .3s ease-in-out;
}

#project:hover{
    box-shadow: rgba(0, 0, 0, 0.22) 0px 19px 43px;
    transform: translate3d(0px, -7px, 0px);
}

span{
    margin-left: 0.5rem;
    font-family: RubikLight;
}

.langs{
    text-transform: uppercase;
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

a{
    color: white !important;
}
</style>