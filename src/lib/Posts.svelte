<script lang="ts">
	import Post from '$lib/Post.svelte';
	export let posts: { path: string; meta: { title: string; date: string } }[];
</script>

<h4 class="ml-8 my-4 text-secondary dark:text-dark-secondary w-auto">Posts</h4>
<ul>
	{#if posts}
		{#each posts as post}
			<Post {post} />
		{/each}
	{/if}
</ul>
