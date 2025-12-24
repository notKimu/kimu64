<script lang="ts">
	type props = {
		title:		string;
		id:			string;
	};

	const props: props = $props();
</script>

<a href="https://youtu.be/{props.id}">
	<div class="video-container">
		<img src="https://img.youtube.com/vi/{props.id}/mqdefault.jpg" alt="Miniatura del vídeo {props.title}">
		<div class="video-container__info">
			<p class="video-container__info__title">{props.title}</p>
		</div>
	</div>
</a>

<style>
	.video-container {
		width:			7rem;
		display:		flex;
		flex-direction:	column;
		gap:			var(--padding-s);
	}

	.video-container__info {
		display:			flex;
		flex-direction:		column;
		flex-wrap:			wrap;
		justify-content:	center;
		gap:				var(--padding-s);
	}

	.video-container__info__title {
		font-size:	small;
	}

	@media screen and (max-width: 728px) {
		.video-container {
			height:			5rem;
			flex-direction:	row;
		}
	}
</style>