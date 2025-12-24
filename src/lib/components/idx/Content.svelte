<script lang="ts">
	// Images
	import ShortcutImage from "$lib/assets/img/shortcut.ico";

	type props = {
		thumbnail_url:	string;
		title:			string;
		link:			string;
	};

	let props: props = $props();
</script>

<a href={props.link}>
	<div class="video-container">
		<div class="video-container__thumbnail">
			<img class="video-container__thumbnail__img" src={props.thumbnail_url} alt={`Miniatura del vídeo ${props.title}`}>
			<img class="video-container__thumbnail__shortcut" src={ShortcutImage} alt="">
		</div>

		<p class="video-container__title">{props.title}</p>
	</div>
</a>

<style>
	.video-container {
		width:				10rem;

		display:			flex;
		flex-direction:		column;
		justify-content:	center;
		align-items:		center;
	}

	.video-container__thumbnail {
		position:	relative;
	}

	.video-container__thumbnail__img {
		width:	100%;
	}

	.video-container__thumbnail__shortcut {
		position:			absolute;
		width:				1.5rem;
		height:				1.5rem;
		right:				-.25rem;
		bottom:				-.25rem;
		image-rendering:	pixelated;
	}

	.video-container__title {
		text-wrap:	wrap;
		text-align:	center;
	}
</style>