<template>
  <div class="my-auto px-4" style="display: table">
    <img
      src="https://media.licdn.com/dms/image/v2/C5603AQG8oikx_4bm_w/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646460298961?e=1741219200&v=beta&t=qwJJRDiuRRbyLQx8kKxKyyAlLU0FnhNDzR15cqJHDjo"
      class="rounded-full mb-4 w-44 h-44"
    />

    <h1 class="text-3xl leading-none font-semibold">Isaias Briones</h1>
    <p class="font-extralight text-gray-400">
      I am an experienced Full-Stack, Mobile, and Software Engineer.
    </p>

    <br />
    <Link
      icon="bx-envelope"
      title="briones@ualberta.ca"
      url="mailto:briones@ualberta.ca"
    />
    <Link icon="bx-phone" title="1 (780) 278 6076" url="sms:+1-780-278-6076" />

    <br />
    <div class="flex">
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
