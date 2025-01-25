<template>
  <h2 class="mb-2 text-xl py-2 text-red-800">GitHub projects!</h2>

  <section v-if="pending">Loading...</section>
  <section v-else-if="error">Error... Try again!</section>
  <section v-else>
    <p class="text-right mb-2 text-blue-600 font-mono">
      Repos: {{ data.length }}
    </p>
    <ul class="grid grid-cols-1 gap-2">
      <li
        v-for="repository in data"
        :key="repository.id"
        class="border border-gray-200 hover:bg-gray-100 dark:hover:bg-gray-700 dark:hover:text-white font-mono overflow-hidden rounded-md"
      >
        <a :href="repository.html_url" target="_blank" class="block p-5">
          <p class="font-medium">{{ repository.name }}</p>
          <p>{{ repository.description }}</p>
        </a>
      </li>
    </ul>
  </section>
</template>

<script setup>
const URL = "https://api.github.com/users/Grinch3214";

const { error, pending, data } = await useFetch(
  `${URL}/repos?per_page=100&page=1`
);
</script>
