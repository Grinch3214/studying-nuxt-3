<template>
	<div class="container mx-auto max-w-2xl">
		<header class="flex justify-between items-center mt-5">
			<div>
				<NuxtLink to="/" class="text-xl font-semibold p-2 hover:bg-gray-200">Max Grinch</NuxtLink>
			</div>
			<nav class="font-mono">
				<ul class="flex space-x-4">
					<li class="mb-2 text-pink-400"><NuxtLink to="/">Main</NuxtLink></li>
					<li><NuxtLink to="/about">About</NuxtLink></li>
				</ul>
			</nav>
		</header>
		<main class="p-2">
			<slot />
		</main>
	</div>
</template>