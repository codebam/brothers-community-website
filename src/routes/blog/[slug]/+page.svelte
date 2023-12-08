<script>
	export let data;
</script>

<svelte:head>
	<title>{data.title}</title>
</svelte:head>
<article>
	<h2>{data.title}</h2>
	<h5>{data.date}</h5>
	<p id="blogpost">{@html data.html}</p>
</article>

<style>
	#blogpost :global(a) {
		text-decoration: underline;
	}
</style>
