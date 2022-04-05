<script lang="ts">
</script>

<!-- DEFINING HTML IN svelte:head BREAKS CSS -->
<svelte:head>
	<html lang="en" />
</svelte:head>

<slot />

<style global>
	@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400&display=swap');

	:root {
		--color1: #00b9ae;
		--color2: #009f93;
		--color3: #037979;
		--color4: #292929;
		--color5: #303030;
		--color6: rgb(59, 59, 59);
		--color7: rgb(77, 77, 77);
		--color8: rgb(73, 73, 73);
		--input-color1: var(--color6);
		--input-color2: var(--color7);
		--input-color3: var(--color8);

		font-family: 'Montserrat', sans-serif;
		color: rgba(255, 255, 255, 0.974);
	}

	body {
		background-color: var(--color3);
		margin: 0;
		padding: 0.6em 1.5em;
		width: 100%;
		box-sizing: border-box;
	}

	@media only screen and (max-width: 768px) {
		body {
			padding: 0em 0.4em;
		}
	}

	ul {
		padding: 0;
		margin: 0;
	}

	input {
		background-color: var(--input-color1);
		color: rgba(255, 255, 255, 0.967);
		border: solid;
		border-width: 2px;
		border-color: var(--color4);
		border-radius: 3px;
	}
	::placeholder {
		color: rgba(255, 255, 255, 0.542);
	}

	input {
		padding: 0.5em;
		font-size: medium;
	}

	input[type='submit']:hover {
		cursor: pointer;
		background-color: var(--input-color2);
	}

	input[type='submit']:active {
		background-color: var(--input-color3);
	}

	textarea {
		background-color: var(--input-color1);
		color: rgba(255, 255, 255, 0.967);
		border: solid;
		border-width: 2px;
		border-color: rgba(38, 38, 38, 0.83);
		border-radius: 3px;
		font-size: large;
		box-sizing: border-box;
	}
</style>
