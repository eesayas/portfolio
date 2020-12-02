<template>
    <div v-show="show">
        <div id="detail-cont" class="w-100 fixed-top">
            <div class="mx-5 my-3">
                <div class="d-flex align-items-center">
                    <h1>classie</h1>
                    <a class="mx-3" style="color: #eedfbb;">VIEW DEMO</a>
                    <a class="ml-auto mr-3" v-on:click="$emit('toggle')" style="color: #eedfbb;">GO BACK</a>
                </div>
            </div>

            <iframe width="80%" id="video-data"
                src="https://www.youtube.com/embed/C9_weFglsAU"
                frameborder="0" allow="accelerometer; autoplay; 
                encrypted-media; gyroscope; picture-in-picture" 
                allowfullscreen>
            </iframe>

            <p>hello</p>



        </div>
    </div>
</template>

<script>
export default {
    name: "ProjectDetail",
    props: ["show"],
}
</script>

<style scoped>
#detail-cont{
    background: #171B1B;
    margin-top: 6.3rem;
}

iframe{
    height: 200rem;
}
</style>