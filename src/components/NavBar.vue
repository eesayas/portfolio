<template>
    <div class="navbar-cont fixed-top">
        <b-navbar toggleable="lg" type="dark">
            <b-navbar-brand href="#">
                <span id="navbar-brand">eesayas.</span>
            </b-navbar-brand>
            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
                <b-navbar-nav class="ml-auto">
                    <b-nav-item href="#" style="color: black;">
                        <span>ABOUT ME</span>
                    </b-nav-item>
                    <b-nav-item href="#">
                        <span>PROJECTS</span>
                    </b-nav-item>
                    <b-nav-item href="#">
                        <span>CONTACT</span>
                    </b-nav-item>
                </b-navbar-nav>
            </b-collapse>
    </b-navbar>
    </div>
</template>

<script>
export default {
    name: "NavBar",
}
</script>

<style scoped>
    .navbar-cont{
        padding: 1rem;
        background-color: #171B1B !important;
    }

    #navbar-brand{
        font-size: 1.8rem !important;
    }

    span{
        font-size: 1.2rem;
        color: #eedfbb !important;
    }
</style>