<template>
  <h2>All posts here (test)</h2>
  <div v-for="item in data">{{ item.title }}</div>
</template>

<script setup>
const { data } = await useAsyncData("blog", () => queryContent("/").find());

console.log(data);
</script>
