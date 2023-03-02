<script setup lang="ts">
const greeting = "Welcome to this site";
let message = 'This site contains information about available jobs.';

const changeMessage = () => {
	message = 'This site also contains skills you need for IT jobs.';
}
</script>

<template>
	<div class="welcome">
		<h2>{{ greeting }}</h2>
		<p>{{ message }}</p>
		<button @click="changeMessage">more info</button>
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