<template>
  <div>All posts here</div>
  <p>TEST page</p>
  <div v-for="item in data">{{ item.title }}</div>
</template>

<script setup>
const { data } = await useAsyncData("blog", () => queryContent("/").find());
</script>
