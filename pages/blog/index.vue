<template>
  <h2 class="font-semibold text-lg">All posts here</h2>
  <div class="flex flex-col gap-3" v-for="item in data">{{ item.title }}</div>
</template>

<script setup>
const { data } = await useAsyncData('blog', () => queryContent('/').find());
console.log(data);
</script>
