<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
// !TODO: Need to recreate
useHead({
  link: [
    {
      rel: "preconnect",
      href: "https://fonts.googleapis.com",
    },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Roboto&display=swap",
      crossorigin: "",
    },
  ],
});
</script>

<style>
body {
  font-family: "Roboto", sans-serif;
  @apply dark:bg-gray-900 bg-white text-gray-700 dark:text-gray-400;
}
</style>
