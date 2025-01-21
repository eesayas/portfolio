<template>
  <div class="flex items-center text-gray-400 text-sm mb-2">
    <i class="bx bx-sm bx-briefcase mr-2"></i>
    {{ props.date }}
    <br />
    {{ props.company }} &#x2022; {{ props.type }}
  </div>
</template>

<script lang="ts" setup>
interface Props {
  date: string;
  company: string;
  type: "Contract" | "Full Time" | "Part Time";
}

const props = defineProps<Props>();
</script>
