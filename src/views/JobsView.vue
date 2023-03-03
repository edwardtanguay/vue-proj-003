<script setup lang="ts">
import type { IJob } from '@/interfaces';
import axios from 'axios';

const jobs: IJob[] = (
	await axios.get('https://edwardtanguay.vercel.app/share/jobs.json')
).data;
</script>

<template>
	<div class="jobs">
		<p>There are {{ jobs.length }} jobs.</p>
		<ul>
			<li v-for="job in jobs">
				<a target="_blank" :href="job.url">{{ job.title }}</a> -
				{{ job.company }}
			</li>
		</ul>
	</div>
</template>

<style scoped>
li {
	color: #ccc;
	font-size: 1.3rem;
}
a {
	color: rgb(218, 218, 128);
}
</style>
