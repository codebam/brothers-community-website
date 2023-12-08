<script lang="ts">
	import Carousel from 'svelte-carousel';
	import { browser } from '$app/environment';
	import Posts from '$lib/Posts.svelte';
	import SearchBar from '$lib/SearchBar.svelte';
	export let data: { posts: { path: string; meta: { title: string; date: string } }[] };
</script>

<div id="topbar">
	<img height="75px" src="/brothers_logo.png" alt="brothers logo" />
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
		<img height="500px" src="/carousel0.jpg" alt="colourful mountains" />
		<img height="500px" src="/carousel1.jpg" alt="dark and raining" />
		<div id="ad">ad goes here <a href="/ad">click</a></div>
	</Carousel>
{/if}
<div id="content">
	<h1>Brothers International Community</h1>
	<h2>Join brothers community</h2>
	<h3>Build trustworthy international connections</h3>
	<Posts posts={data.posts} />
</div>
<footer>
	<p>
		<a href="mailto:brotherscommunityinternational@gmail.com"> Email </a>
		<a href="https://t.me/Brothers_in_law"> Telegram </a>
	</p>
</footer>

<style>
	#topbar {
		display: flex;
		justify-content: space-between;
	}
	#ad {
		text-align: center;
	}
	#content {
		text-align: center;
	}
	footer {
		display: flex;
		justify-content: space-around;
	}
</style>
