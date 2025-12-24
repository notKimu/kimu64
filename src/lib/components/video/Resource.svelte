<script lang="ts">
	type props = {
		name:	string;
		url:	string;
	};

	const props: props = $props();

	const origin = URL.parse(props.url)?.origin;
</script>

<a href={props.url} target="_blank">
	<div class="resource-container">
		<img src="https://s2.googleusercontent.com/s2/favicons?domain={origin}" alt="{props.name} favicon">
		<p>{props.name}</p>
	</div>
</a>

<style>
	.resource-container {
		display:		flex;
		flex-direction:	row;
		align-items:	center;
		gap:			var(--padding-s);
	}

	.resource-container img {
		height:			1.5rem;
	}
</style>