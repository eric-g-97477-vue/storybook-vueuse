<script setup lang="ts">
	// import HelloWorld from './components/HelloWorld.vue';
	// import TheWelcome from './components/TheWelcome.vue';
	import Button from './stories/Button.vue';

	import { useDark, useToggle } from '@vueuse/core';

	const isDark = useDark();

	function togglemode() {
		isDark.value = !isDark.value;
		console.log('Toggle Mode', isDark.value);
	}
</script>

<template>
	<button @click="togglemode">Toggle</button>
	<Button label="Report Mode" :primary="true"></Button>
</template>

<style scoped></style>
