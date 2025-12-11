<template>
  <div class="container mx-auto max-w-[1200px]">
    <header class="flex justify-between items-center mt-5">
      <div class="flex items-center gap-4 w-full">
        <NuxtLink
          to="/"
          class="text-2xl font-bold py-2 px-4 hover:text-gray-200"
          >Max Grinch</NuxtLink
        >
        <Menu class="ml-auto my-2" />
        <ColorModeSelector />
      </div>
    </header>
    <main class="p-2 mt-4">
      <slot />
    </main>
  </div>
</template>
