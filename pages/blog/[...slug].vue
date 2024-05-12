<template>
  <article
    class="prose dark:prose-invert prose-pre:bg-white dark:prose-pre:bg-gray-800"
  >
    <ContentDoc />
  </article>
</template>

<script setup>
const route = useRoute();
console.log(route.params.slug);
</script>
