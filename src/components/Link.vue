<template>
  <span class="flex items-center">
    <i class="bx bx-sm" :class="{ [props.icon]: true }"></i>
    <a class="mx-2 font-light" role="button" target="_blank" :href="props.url">
      {{ props.title }}
    </a>
  </span>
</template>

<script setup lang="ts">
interface Props {
  url: string;
  title: string;
  icon: string;
}

const props = defineProps<Props>();
</script>
