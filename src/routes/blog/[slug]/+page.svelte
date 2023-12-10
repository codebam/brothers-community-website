<script>
	import TopBar from '$lib/TopBar.svelte';
	export let data;
</script>

<svelte:head>
	<title>{data.title}</title>
</svelte:head>
<TopBar data={{ posts: [] }} />
<article>
	<h2>{data.title}</h2>
	<div id="blogpost">{@html data.html}</div>
</article>

<style>
	#blogpost :global(a) {
		text-decoration: underline;
	}
	article {
		margin: 1rem;
	}
</style>
