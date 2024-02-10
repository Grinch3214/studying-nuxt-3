<template>
	<div class="mb-2 text-xl py-2 text-red-800">Projects</div>
	<section v-if="pending">Loading...</section>
	<section v-else-if="error">Wrong... Try again!</section>
	<section v-else>Here we display the repos!</section>
</template>

<script setup>
const { error, pending, data } = await useFetch('https://api.github.com/users/Grinch3214/repos')
</script>