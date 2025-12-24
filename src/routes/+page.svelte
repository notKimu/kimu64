<script lang="ts">
	import Content	from "$lib/components/idx/Content.svelte";
	import Title	from "$lib/components/idx/Title.svelte";
	import Window	from "$lib/components/Window.svelte";
</script>

<div class="main-container">
	<div class="main-container__logo">
		<Window title="Name" app="Word">
			<div class="main-container__logo__content">
				 <Title text="Kimu_x64" />
			</div>
		</Window>
	</div>

	<div class="main-container__content">
		<div class="main-container__videos">
			<Window title="Videos" app="Word">
				<div class="main-container__videos__list">
					<Content
						thumbnail_url="https://i3.ytimg.com/vi/xsQglFTieUc/maxresdefault.jpg"
						title="Reviviendo tus Cacharritos con Linux"
						link="rtccl"
					/>
				</div>
			</Window>
		</div>
	
		<div class="main-container__updates">
			<Window title="Updates" app="Word">
				<div class="main-container__updates__list">
					<p>Breaking News: Pitito</p>
					<p>Update: Tres Tres Tres Tres Tres Tres Tres Tres Tres Tres</p>
				</div>
			</Window>
		</div>
	</div>
</div>

<style>
	.main-container {
		display:		flex;
		flex-direction:	column;
		gap:			var(--padding-x);
	}

	.main-container__logo__content {
		display:			flex;
		justify-content:	center;
		align-items:		center;
		padding: 0;
	}

	.main-container__content {
		width:			100%;
		display:		flex;
		flex-direction:	row;
		gap:			var(--padding-x);
	}

	.main-container__videos {
		width:	100%;
	}

	.main-container__videos__list {
		display:	flex;
		flex-wrap:	wrap;
		gap:		var(--padding-x);
	}

	.main-container__updates {
		 width:	clamp(32rem, 30vw, 50rem);
	}

	.main-container__updates__list {
		display:		flex;
		flex-direction:	column;
		gap:			var(--padding-x);
	}

	@media screen and (max-width: 728px) {
		.main-container__content {
			flex-direction:	column;
		}

		.main-container__updates {
			width:	100%;
		}
	}
</style>