<script setup lang="ts">
import axios from 'axios';
const jobs = (await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')).data;
</script>

<template>
	<div class="jobs">
		<p>There are {{ jobs.length }} jobs.</p>
	</div>
</template>
