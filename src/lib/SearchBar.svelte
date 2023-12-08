<script lang="ts">
	import { afterUpdate } from 'svelte';
	import Fuse from 'fuse.js';
	let search = '';
	export let posts;
	let results = posts;
	const options = { keys: ['meta.title'] };
	const fuse = new Fuse(posts, options);
	afterUpdate(() => {
		results = fuse.search(search);
		results = results.map((item: any) => ({ path: item.item.path, title: item.item.meta.title }));
	});
</script>

<div>
	<input bind:value={search} placeholder="search" />
	{#if results.length !== 0}
		<ul>
			{#each results as result}
				<li><a href={result.path}>{result.title}</a></li>
			{/each}
		</ul>
	{/if}
</div>

<style>
	input {
		height: 1em;
		border-radius: 1rem;
		padding: 0.5rem;
		margin-top: 0.1em;
		background-color: #2e3440;
		color: white;
		border-width: 0;
	}
</style>
