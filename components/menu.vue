<template>
  <nav>
    <ul class="flex space-x-4 items-center">
      <li v-for="link in links" :key="link.id">
        <NuxtLink
          :to="link.path"
          class="hover:text-zinc-400 transition-opacity"
        >
          {{ link.name }}
        </NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<script setup lang="ts">
interface Link {
  id?: number;
  name?: string;
  path?: string;
}
const links = [
  { id: 1, name: "Main", path: "/" },
  { id: 2, name: "About", path: "/about" },
  { id: 3, name: "Projects", path: "/projects" },
  { id: 4, name: "Blog", path: "/blog" },
] as Link[];
</script>
