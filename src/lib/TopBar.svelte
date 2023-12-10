<script lang="ts">
	import SearchBar from '$lib/SearchBar.svelte';
	export let data: { posts: { path: string; meta: { title: string; date: string } }[] };
</script>

<div id="topbar">
	<a href="/"><img height="32px" src="/brothers_logo.png" alt="brothers logo" /></a>
	<SearchBar posts={data.posts} />
</div>

<style>
	#topbar {
		display: flex;
		justify-content: space-between;
		height: 4rem;
		padding-top: 2rem;
		padding-left: 1rem;
		padding-right: 1rem;
		background-color: #3b4252;
		margin-bottom: 1em;
	}
</style>
