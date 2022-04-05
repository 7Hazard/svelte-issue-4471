<script lang="ts">
	import { goto } from '$app/navigation';
	import { fly } from 'svelte/transition';

	let email: string;
	let password: string;
	function signin(ev: SubmitEvent) {
		ev.preventDefault();
		goto("/timereport")
	}
</script>

<svelte:head>
	<!-- <html lang="en" /> -->
	<title>Login</title>
</svelte:head>

<form on:submit={signin} in:fly={{ y: -10, duration: 700 }}>
	<h1>Login</h1>
	<input type="text" placeholder="Email" bind:value={email} />
	<input type="password" placeholder="Password" bind:value={password} />
	<input type="submit" value="Sign In" style="margin-top: 0.6em" />
</form>

<style>
	form {
		background-color: var(--color5);

		padding: 1em 2em 2em 2em;
		margin: 5vh auto;
		width: fit-content;

		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		gap: 0.1em;

		border-radius: 4px;
	}
</style>
