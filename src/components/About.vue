<template>
  <div class="my-auto px-4" style="display: table">
    <img
      src="https://media.licdn.com/dms/image/v2/C5603AQG8oikx_4bm_w/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646460298961?e=1741219200&v=beta&t=qwJJRDiuRRbyLQx8kKxKyyAlLU0FnhNDzR15cqJHDjo"
      class="rounded-full mb-4 w-36 h-36"
    />

    <h1 class="text-3xl leading-none font-semibold">Isaias Briones</h1>
    <p class="font-extralight text-gray-400">
      I am a Full-Stack, Mobile, and Software Engineer with a passion for
      coding. My experience includes personal projects, freelance work, and
      professional roles at Dotdash Meredith and the University of Alberta.
    </p>

    <br />

    <Work
      date="05/2021 - 09/2024"
      company="Dotdash Meredith"
      type="Full Time"
    />
    <Work
      date="06/2021 - 09/2021"
      company="University of Alberta"
      type="Contract"
    />
    <div href="#" class="text-sm text-gray-400 underline cursor-pointer">
      Read Resume
    </div>
    <br />

    <div class="text-sm">
      <h6 class="mb-1">Contact Info</h6>
      <Link
        v-for="(link, index) of links"
        :key="index"
        v-bind="link"
        class="mb-1"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import Link from "./Link.vue";
import Work from "./Work.vue";

const links = [
  {
    title: "briones@ualberta.ca",
    icon: "bx-envelope",
    url: "https://github.com/eesayas",
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
