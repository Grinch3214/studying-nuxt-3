<template>
  <div>All posts here</div>
  <p>{{ data }}</p>
</template>

<script setup>
const { data } = await useAsyncData("blog", () => queryContent("/").find());
</script>
