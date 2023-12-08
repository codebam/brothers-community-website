<script lang="ts">
	import Post from '$lib/Post.svelte';
	export let posts: { path: string; meta: { title: string; date: string } }[];
</script>

<h4>Posts</h4>
<ul>
	{#if posts}
		{#each posts as post}
			<Post {post} />
		{/each}
	{/if}
</ul>
