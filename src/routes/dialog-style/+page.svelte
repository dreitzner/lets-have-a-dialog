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
		<br>
		<br>
		<button type="submit">Submit</button>
		<a href="/">Close</a>
	</form>
</dialog>

<style>
	dialog {
		height: 50vh;
		width: 50vw;
		border-color: lime;
	}
	dialog::backdrop {
		background-color: rgba(255, 192, 203, 0.5);
	}
</style>
