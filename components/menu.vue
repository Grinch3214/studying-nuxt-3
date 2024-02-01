
<template>
	<nav class="font-mono">
		<ul class="flex space-x-4">
			<li class="mb-2 text-pink-400">
				<NuxtLink to="/" class="link">Main</NuxtLink>
			</li>
			<li>
				<NuxtLink to="/about" class="link">About</NuxtLink>
			</li>
		</ul>
	</nav>
</template>

<style scoped>
	.link {
		@apply p-1 hover:bg-gray-200;
	}
</style>