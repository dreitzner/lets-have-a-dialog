<script>
    import { onMount } from "svelte";

	/**
	 * @type {HTMLDialogElement}
	 */
	let dialog;

	onMount(() => {
		dialog.showModal();
	})
</script>

<dialog bind:this={dialog}>
	<form method="dialog">
		<h1>Hi Svienna</h1>
		<label for="email">enter email</label>
		<input type="email" name="email" id="email">
		<button type="submit">Submit</button>
		<a href="/">Close</a>
	</form>
</dialog>

<style>
</style>
