<template>
  <div>
    <article
      class="prose mx-auto dark:prose-invert prose-pre:bg-white dark:prose-pre:bg-gray-800 prose-pre:text-gray-700 dark:prose-pre:text-gray-200 w-full"
    >
      <ContentDoc />
    </article>
  </div>
</template>

<script setup>
const route = useRoute();

console.log(route);
</script>
