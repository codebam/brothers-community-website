<!-- 
	Brothers website admin panel
	see: https://kit.svelte.dev/docs/form-actions
	we can either put the backend in form actions or connect to our backend there
-->

<form method="POST" action="?/admin/add">
	<div id="add-admin">
		<label for="name">Add admin: </label>
		<input type="text" name="username" id="username" required />
		<input type="text" name="permissions" id="permissions" required />
	</div>
	<input type="submit" />
</form>

<form method="POST" action="?/admin/remove">
	<div id="remove-admin">
		<label for="name">Remove admin: </label>
		<input type="text" name="username" id="username" required />
	</div>
	<input type="submit" />
</form>

<form method="POST" action="?/post/add">
	<div id="add-post">
		<label for="name">Add post: </label>
		<input type="text" name="content" id="content" required />
		<input type="text" name="tags" id="tags" required />
	</div>
	<input type="submit" />
</form>

<form method="POST" action="?/post/remove">
	<div id="remove-post">
		<label for="name">Remove post: </label>
		<input type="text" name="postid" id="postid" required />
	</div>
	<input type="submit" />
</form>
