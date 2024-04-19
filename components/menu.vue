
<template>
	<nav class="font-mono">
		<ul class="flex space-x-4 items-center">
			<li>
				<NuxtLink to="/" class="link active">Main</NuxtLink>
			</li>
			<li>
				<NuxtLink to="/about" class="link">About</NuxtLink>
			</li>
			<li>
				<NuxtLink to="/projects" class="link">Projects</NuxtLink>
			</li>
		</ul>
	</nav>
</template>

<style scoped>
	.link {
		@apply p-1 hover:text-gray-500;
	}
	.link.active {
		@apply text-blue-400;
	}
</style>