<template>
	<div class="mb-2 text-2xl py-2 text-gray-800">Projects</div>
</template>

<script setup>
console.log(await $fetch('https://api.github.com/users/Grinch3214/repos'))
</script>