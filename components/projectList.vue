<template>
	<p class="mb-2 text-xl py-2 text-red-800">Take a look at my GitHub projects!</p>

	<section v-if="pending">Loading...</section>
	<section v-else-if="error">Error... Try again!</section>
	<section v-else>
		<ul class="grid grid-cols-1 gap-4">
			<li
				v-for="repository in data"
				:key="repository.id"
				class="border border-gray-200 rounded-sm hover:bg-gray-100 font-mono overflow-hidden"
			>
				<a :href="repository.html_url" target="_blank" class="block p-4">
					<div class="font-semibold"> {{ repository.name }} </div>
					<div>{{ repository.description }}</div>
				</a>
			</li>
		</ul>
	</section>
</template>

<script setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/Grinch3214/repos')
</script>