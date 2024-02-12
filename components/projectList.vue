<template>
	<p class="mb-2 text-xl py-2 text-red-800">Take a look at my GitHub projects!</p>

	<section v-if="pending">Loading...</section>
	<section v-else-if="error">Error... Try again!</section>
	<section v-else>
		<ul class="grid grid-cols-1 gap-4">
			<li
				v-for="repository in data"
				:key="repository.id"
				class="border border-gray-200 rounded-sm p-4 hover:bg-gray-100 font-mono"
			>
				<a :href="repository.html_url" target="_blank">
					<div class="font-semibold"> {{ repository.name }} </div>
				</a>
				<p>{{ repository.tags_url }}</p>
			</li>
		</ul>
	</section>
</template>

<script setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/Grinch3214/repos')
</script>