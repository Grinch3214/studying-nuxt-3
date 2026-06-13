<template>
  <a :href="repository.html_url" target="_blank">
    <p class="font-medium text-base">{{ repository.name }}</p>
    <p class="text-sm">{{ repository.description }}</p>
  </a>
</template>

<script setup lang="ts">
interface Repository {
  html_url: string;
  name: string;
  description: string;
}

const props = defineProps<{
  repository: Repository;
}>();
</script>
