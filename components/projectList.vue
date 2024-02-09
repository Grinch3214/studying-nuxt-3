<template>
	<div class="mb-2 text-xl py-2 text-red-800">
		<p v-for="item in projects" :key="item.id">{{ item.name }}</p>
	</div>
</template>

<script setup>
const projects = await $fetch('https://api.github.com/users/Grinch3214/repos')
</script>