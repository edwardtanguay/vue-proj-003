<script setup lang="ts">
const greeting = "Welcome to this site";
const message = 'This site contains information about available jobs.';
</script>

<template>
	<div class="welcome">
		<h2>{{ greeting }}</h2>
		<p>{{ message }}</p>
	</div>
</template>

<style scoped>
	h2 {
		color: orange;
	}

	p {
		color: #aaa;
		font-style: italic;
	}
</style>