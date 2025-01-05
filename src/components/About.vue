<template>
  <div class="my-auto px-4" style="display: table">
    <img
      src="https://media.licdn.com/dms/image/v2/C5603AQG8oikx_4bm_w/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646460298961?e=1741219200&v=beta&t=qwJJRDiuRRbyLQx8kKxKyyAlLU0FnhNDzR15cqJHDjo"
      class="rounded-circle mb-4"
      height="150"
    />

    <h1 class="fs-1 lh-1">Isaias Briones</h1>
    <p class="fw-light text-white-50">
      I am an experienced Full-Stack, Mobile, and Software Engineer.
    </p>
    <Link
      icon="bx-envelope"
      title="briones@ualberta.ca"
      url="mailto:briones@ualberta.ca"
    />
    <Link icon="bx-phone" title="1 (780) 278 6076" url="sms:+1-780-278-6076" />

    <br />
    <div class="d-flex">
      <Link v-for="(link, index) of links" :key="index" v-bind="link" />
    </div>
  </div>
</template>

<script setup lang="ts">
import Link from "./Link.vue";

const links = [
  {
    title: "Resume",
    icon: "bx-file",
    url: "https://www.canva.com/design/DAEDwiJGzjk/LFpSj0awI-DiSK9Q3f0jkw/view?utm_content=DAEDwiJGzjk&utm_campaign=designshare&utm_medium=link&utm_source=sharebutton",
  },
  {
    title: "Github",
    icon: "bxl-github",
    url: "https://github.com/eesayas",
  },
  {
    title: "LinkedIn",
    icon: "bxl-linkedin-square",
    url: "https://www.linkedin.com/in/eesayas/",
  },
];
</script>
