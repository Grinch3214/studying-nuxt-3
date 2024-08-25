<template>
  <div>All posts here</div>
</template>

<script setup>
const { data } = await useAsyncData("blog", () => queryContent("/").find());
console.log(data.value);
</script>
