<script lang="ts">
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import Posts from '$lib/Posts.svelte';
	import SearchBar from '$lib/SearchBar.svelte';
	export let data: { posts: { path: string; meta: { title: string; date: string } }[] };
	let carousel;
</script>

<img width="100px" src="/brothers_logo.png" alt="brothers logo" />
<SearchBar posts={data.posts} />
{#if browser}
	<Carousel bind:this={carousel}>
		<img src="/carousel0.jpg" alt="colourful mountains" />
		<img src="/carousel1.jpg" alt="dark and raining" />
	</Carousel>
{/if}
<h1>Brothers International Community</h1>
<p>
	<a href="mailto:brotherscommunityinternational@gmail.com">
		brotherscommunityinternational@gmail.com
	</a>
</p>
<h4>Join brothers community</h4>
<h5>Build trustworthy international connections</h5>
<Posts posts={data.posts} />
