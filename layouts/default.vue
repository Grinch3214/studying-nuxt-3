<template>
  <div class="container mx-auto max-w-[1200px]">
    <header class="flex justify-between items-center mt-5">
      <div class="flex items-center gap-4 w-full">
        <div>
          <NuxtLink
            to="/"
            class="text-xl font-bold py-2 px-4 hover:text-gray-300"
            >Max</NuxtLink
          >
        </div>
        <Menu class="ml-auto my-3" />
        <ColorModeSelector />
      </div>
    </header>
    <main class="p-2 mt-3">
      <slot />
    </main>
  </div>
</template>
