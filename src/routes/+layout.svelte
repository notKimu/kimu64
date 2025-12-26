<script lang="ts">
	import favicon	from	"$lib/assets/favicon.svg";
	import					"$lib/assets/globals.css";

	let { children } = $props();
</script>

<svelte:head>
	<title>Kimu x64</title>
	<link rel="icon" href={favicon} />
</svelte:head>

<main>
	{@render children()}
</main>
