<template>
  <div>
    <article class="prose-custom">
      <ContentDoc />
    </article>
  </div>
</template>

<style scoped>
.prose-custom {
  @apply prose mx-auto dark:prose-invert prose-pre:bg-white dark:prose-pre:bg-gray-700 prose-pre:text-gray-700 dark:prose-pre:text-gray-300 w-full;
}
</style>
