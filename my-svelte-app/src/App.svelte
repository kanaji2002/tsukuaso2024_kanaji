<script>
	export let name;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>

	

	<!-- SMUI Styles -->
<link
rel="stylesheet"
href="node_modules/svelte-material-ui/themes/svelte.css"
media="(prefers-color-scheme: light)"
/>
<link
rel="stylesheet"
href="node_modules/svelte-material-ui/themes/svelte-dark.css"
media="screen and (prefers-color-scheme: dark)"
/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}


	

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

