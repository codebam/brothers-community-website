<script lang="ts">
	export let post: { path: string; meta: { title: string; date: string } };
</script>

<li>
	<a href={post.path}>
		{post.meta.title}
	</a>
</li>
