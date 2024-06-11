<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between items-center mt-5">
      <div class="flex items-center gap-4 w-full">
        <div>
          <NuxtLink
            to="/"
            class="text-xl font-semibold py-2 px-3 hover:text-gray-400"
            >Max</NuxtLink
          >
        </div>
        <Menu class="ml-auto" />
        <ColorModeSelector />
      </div>
    </header>
    <main class="p-2 mt-3">
      <slot />
    </main>
  </div>
</template>
