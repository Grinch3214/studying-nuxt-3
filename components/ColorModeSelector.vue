<template>
	<div class="flex items-center">
		<button @click="toggleMode">
			{{ nexModeIcon }}
		</button>
	</div>
</template>

<script setup>
	const colorMode = useColorMode()

	const modes = [
		'light',
		'dark'
	]

	const nextModeIcons = {
		light: '🌕',
		dark: '🌑'
	}

	const nextMode = computed(() => {
		const currentModeIndex = modes.indexOf(colorMode.preference)
		let nextModeIndex = null
		currentModeIndex + 1 === modes.length
			? nextModeIndex = 0
				: nextModeIndex = currentModeIndex + 1

		return modes[nextModeIndex]
	})

	const nexModeIcon = computed(() => nextModeIcons[nextMode.value])

	const toggleMode = () => colorMode.preference = nextMode.value
</script>