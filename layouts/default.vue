<template>
	<div class="container mx-auto max-w-2xl">
		<header class="flex justify-between items-center mt-5">
			<div>
				<NuxtLink to="/" class="text-xl font-semibold p-2 hover:text-gray-300">Max</NuxtLink>
			</div>
			<Menu />
		</header>
		<main class="p-2 mt-3">
			<slot />
		</main>
	</div>
</template>

<script setup>
	const colorMode = useColorMode()
</script>
