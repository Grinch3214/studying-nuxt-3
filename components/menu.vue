<template>
  <nav>
    <ul class="flex space-x-4 items-center">
      <li v-for="link in links" :key="link.name">
        <NuxtLink :to="link.path" class="hover:text-zinc-400">{{
          link.name
        }}</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script setup>
const links = [
  { name: "Main", path: "/" },
  { name: "About", path: "/about" },
  { name: "Projects", path: "/projects" },
];
</script>
