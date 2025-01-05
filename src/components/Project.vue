<template>
  <div id="project" class="px-5 py-4 my-3 user-select-none" role="button">
    <div class="d-flex flex-wrap">
      <div
        v-for="(tech, index) in props.stack"
        :key="index"
        class="text-uppercase d-flex align-items-center me-2 mb-1 flex-nowrap"
      >
        <img :src="icon(tech)" height="20" width="20" class="me-1" />
        {{ tech }}
      </div>
    </div>
    <h2>{{ props.name }}</h2>
    <p class="text-white-50 fw-lighter">{{ props.description }}</p>

    <div class="d-flex">
      <Link
        title="Code"
        icon="bx-code"
        :url="props.code"
        v-if="props.code"
        class="me-2"
      />
      <Link
        title="View App"
        icon="bx-desktop"
        :url="props.app"
        v-if="props.app"
        class="me-2"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import Link from "./Link.vue";
import { computed } from "vue";

export interface Props {
  stack: string[];
  name: string;
  description: string;
  code?: string;
  app?: string;
}

const props = defineProps<Props>();

const icons: Record<string, string> = {
  vue: "https://vuejs.org/logo.svg",
  pinia: "https://pinia.vuejs.org/logo.svg",
  svelte: "https://svelte.dev/favicon.png",
  nuxt: "https://nuxt.com/icon.png",
  vuetify: "https://vuetifyjs.com/favicon.ico",
  bootstrap: "https://getbootstrap.com/favicon.ico",
  expressjs: "https://expressjs.com/images/favicon.png",
  webrtc: "https://webrtc.org/favicon.ico",
  python: "https://www.python.org/favicon.ico",
  deno: "https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Deno_Logo_2024.svg/240px-Deno_Logo_2024.svg.png",
  tensorflow:
    "https://upload.wikimedia.org/wikipedia/commons/thumb/2/2d/Tensorflow_logo.svg/115px-Tensorflow_logo.svg.png",
  tailwind: "https://tailwindcss.com/favicons/favicon.ico?v=3",
  nestjs: "https://nestjs.com/favicon.fe097249.ico",
  turborepo: "https://turbo.build/images/product-icons/repo-light-32x32.png",
  react: "https://react.dev/favicon.ico",
};

const icon = computed(() => (tech: string) => {
  return icons[tech.toLowerCase()] || `https://${tech}.com/favicon.ico`;
});
</script>

<style scoped>
#project {
  background: #202022;
  transition: all 0.3s ease-in-out;
}

#project:hover {
  box-shadow: rgba(0, 0, 0, 0.22) 0px 19px 43px;
  transform: translate3d(0px, -7px, 0px);
}
</style>
