<script lang="ts">
	export let post: { path: string; meta: { title: string; date: string } };
</script>

<li>
	<h5>
		<a href={post.path}>
			{post.meta.title}
		</a>
	</h5>
</li>
