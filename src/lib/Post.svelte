<script lang="ts">
	export let post: { path: string; meta: { title: string; date: string } };
</script>

<li
	class="bg-background-secondary dark:bg-dark-background-secondary m-2
        py-4 pr-4 drop-shadow border-2 border-background-tertiary dark:border-dark-background-tertiary
        rounded-3xl hover:border-quaternary hover:dark:border-dark-quaternary w-auto"
>
	<h5 class="underline text-primary dark:text-dark-primary ml-8 w-auto">
		<a class="hover:text-tertiary dark:hover:text-dark-tertiary" href={post.path}>
			{post.meta.title}
		</a>
	</h5>
</li>
