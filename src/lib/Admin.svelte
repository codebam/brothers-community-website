<!-- 
	Brothers website admin panel
	see: https://kit.svelte.dev/docs/form-actions
	we can either put the backend in form actions or connect to our backend there
-->

<h3>Add Admin</h3>
<form method="POST" action="?/admin/add">
	<div id="add-admin">
		<label for="username">Username: </label>
		<input type="text" name="username" id="username" required />
		<label for="permissions">Permissions: </label>
		<input type="text" name="permissions" id="permissions" required />
	</div>
	<input type="submit" />
</form>

<h3>Remove Admin</h3>
<form method="POST" action="?/admin/remove">
	<div id="remove-admin">
		<label for="username">Username: </label>
		<input type="text" name="username" id="username" required />
	</div>
	<input type="submit" />
</form>

<h3>Add post</h3>
<form method="POST" action="?/post/add">
	<div id="add-post">
		<label for="content">Content: </label>
		<input type="text" name="content" id="content" required />
		<label for="tags">Tags: </label>
		<input type="text" name="tags" id="tags" required />
	</div>
	<input type="submit" />
</form>

<h3>Remove post</h3>
<form method="POST" action="?/post/remove">
	<div id="remove-post">
		<label for="postid">Post ID: </label>
		<input type="text" name="postid" id="postid" required />
	</div>
	<input type="submit" />
</form>
