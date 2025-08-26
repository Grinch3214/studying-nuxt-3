<template>
  <h2 class="mb-2 text-xl py-2 text-red-600">GitHub projects!</h2>

  <section v-if="pending">Loading...</section>
  <section v-else-if="error">Error... Try again!</section>
  <section v-else>
    <h3 class="text-right mb-2 text-blue-600 font-mono">
      Repos: {{ data.length }}
    </h3>
    <ul class="grid grid-cols-1 gap-2">
      <li
        v-for="repository in data"
        :key="repository.id"
        class="border border-gray-500 hover:bg-gray-200 dark:hover:bg-gray-600 dark:hover:text-white font-mono overflow-hidden rounded-md"
      >
        <projectItem
          :repository="repository"
          :id="repository.id"
          class="block p-2"
        />
      </li>
    </ul>
  </section>
</template>

<script setup>
const URL = 'https://api.github.com/users/Grinch3214';

const { error, pending, data } = await useFetch(
  `${URL}/repos?per_page=100&page=1`
);
</script>
