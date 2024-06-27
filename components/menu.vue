<template>
  <nav>
    <ul class="flex space-x-4 items-center">
      <li v-for="link in links" :key="link.id">
        <NuxtLink :to="link.path" class="hover:text-zinc-400">{{
          link.name
        }}</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script setup>
const links = [
  { id: 1, name: "Main", path: "/" },
  { id: 2, name: "About", path: "/about" },
  { id: 3, name: "Projects", path: "/projects" },
];
</script>
