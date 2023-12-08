<script lang="ts">
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import Posts from '$lib/Posts.svelte';
	import SearchBar from '$lib/SearchBar.svelte';
	export let data: { posts: { path: string; meta: { title: string; date: string } }[] };
</script>

<div id="topbar">
	<img height="32px" src="/brothers_logo.png" alt="brothers logo" />
	<SearchBar posts={data.posts} />
</div>
{#if browser}
	<Carousel
		timingFunction="linear"
		swiping={false}
		arrows={false}
		dots={false}
		autoplay={true}
		autoplayDuration={5000}
	>
		<img src="/carousel0.jpg" alt="colourful mountains" />
		<img src="/carousel1.jpg" alt="dark and raining" />
	</Carousel>
{/if}
<div id="content">
	<h1>Brothers International Community</h1>
	<h2>Join brothers community</h2>
	<h3>Build trustworthy international connections</h3>
	<Posts posts={data.posts} />
</div>
<footer>
	<div id="contact">
		<a href="mailto:brotherscommunityinternational@gmail.com">
			<img src="/email.svg" alt="email" width="50px" /></a
		>
		<a href="https://t.me/Brothers_in_law"
			><img src="/telegram.svg" alt="telegram" width="50px" /></a
		>
	</div>
</footer>

<style>
	h1 {
		color: #8fbcbb;
	}
	h2 {
		color: #88c0d0;
	}
	h3 {
		color: #81a1c1;
	}
	img {
		border-radius: 0.5rem;
	}
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
	#content {
		text-align: center;
	}
	#contact {
		display: flex;
		justify-content: space-around;
	}
</style>
