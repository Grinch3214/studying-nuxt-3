<template>
  <div>All posts here</div>
  <p>TEST page</p>
  <div v-for="item in data">{{ item.title }}</div>
  <pre>{{ data }}</pre>
</template>

<script setup>
const { data } = await useAsyncData("blog", () => queryContent("/").find());
</script>
