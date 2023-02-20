<script>
    import { onMount } from "svelte";
	import clickOutside from '@svackages/click-outside-action';
    import { goto } from "$app/navigation";

	/**
	 * @type {HTMLDialogElement}
	 */
	let dialog;

	onMount(() => {
		dialog.showModal();
	})

	const close = () => goto('/')
	
</script>

<dialog bind:this={dialog} on:close={close}>
	<form method="dialog" use:clickOutside={close}>
		<h1>Hi Svienna</h1>
		<label for="email">enter email</label>
		<input type="email" name="email" id="email">
		<button type="submit">Submit</button>
		<a href="/">Close</a>
	</form>
</dialog>

<style>
</style>
