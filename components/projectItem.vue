<template>
  <a :href="repository.html_url" target="_blank">
    <p class="font-medium text-base">{{ repository.name }}</p>
    <p class="text-sm">{{ repository.description }}</p>
  </a>
</template>

<script setup lang="ts">
const props = defineProps<{
  repository: any;
}>();
</script>
