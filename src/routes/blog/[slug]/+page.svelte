<script>
	export let data;
</script>

<svelte:head>
	<title>{data.title}</title>
	<link rel="stylesheet" href="/prism.css" />
	<link rel="stylesheet" href="https://latest.cactus.chat/style.css" type="text/css" />
</svelte:head>
<article>
	<h2 class="text-secondary dark:text-dark-secondary">{data.title}</h2>
	<h5 class="text-secondary dark:text-dark-secondary">{data.date}</h5>
	<p id="blogpost" class="my-4 text-secondary dark:text-dark-secondary">{@html data.html}</p>
	<div id="comment-section"></div>
</article>

<style>
	#blogpost :global(a) {
		text-decoration: underline;
	}
</style>
