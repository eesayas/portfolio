<template>
  <div class="my-auto px-4" style="display: table">
    <img src="/profile.jpeg" class="rounded-full mb-4 w-36 h-36" />

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
    <Work
      date="08/2015 - 04/2024"
      company="Kumon Canada Inc."
      type="Part Time"
    />
    <div>
      <a
        href="/resume.pdf"
        class="text-sm !text-gray-400 underline cursor-pointer"
        target="_blank"
      >
        Read Resume
      </a>
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
    url: "mailto:briones@ualberta.ca",
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
