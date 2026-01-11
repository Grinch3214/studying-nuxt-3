<template>
  <h2>All posts here</h2>
  <div class="grid gap-3" v-for="item in data">{{ item.title }}</div>
</template>

<script setup>
const { data } = await useAsyncData('blog', () => queryContent('/').find());
</script>
