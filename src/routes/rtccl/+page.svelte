<script lang="ts">
  import Resource	from "$lib/components/video/Resource.svelte";
  import Video 		from "$lib/components/video/Video.svelte";
  import Window		from "$lib/components/Window.svelte";	
</script>

<div class="main-container">
	<Window title="Reviviendo tus Cacharritos con Linux" app="YouTube">
		<div class="main-container__title">
			<h1>Reviviendo Cacharritos</h1>
		</div>
	</Window>

	<div class="main-container__content">
		<Window title="Resources" app="Internet Explorer">
			<div class="main-container__content__resources">
				<div>
					<p>Apps</p>
					<Resource name="Termux" url="https://termux.dev" />
				</div>
				<div>
					<p>Emuladores</p>
					<Resource name="PS1 | DuckStation" url="https://duckstation.org" />
					<Resource name="PS2 | PCSX2" url="https://pcsx2.net" />
					<Resource name="PS2 | NetherSX2" url="https://github.com/Trixarian/NetherSX2-patch" />
					<Resource name="NDS | MelonDS" url="https://melonds.kuribo64.net" />
					<Resource name="3DS | Azahar" url="https://azahar-emu.org" />
					<Resource name="GBA | mGBA" url="https://mgba.io" />
					<Resource name="Xbox | Xemu" url="https://xemu.app" />
					<Resource name="360 | Xenia" url="https://xenia.jp" />
					<Resource name="Retroarch" url="https://www.retroarch.com" />
				</div>
				<div>
					<p>Guías</p>
					<Resource name="Instala Batocera" url="https://wiki.batocera.org/install_batocera" />
					<Resource name="PS2 | Modding" url="https://consolemods.org/wiki/PS2:PS2_Mods_Wiki" />
					<Resource name="360 | Modding" url="https://consolemods.org/wiki/Xbox_360:Xbox_360_Mods_Wiki" />
					<Resource name="NDS | Modding" url="https://wiki.ds-homebrew.com/ds-index" />
					<Resource name="DSI | Modding" url="https://dsi.cfw.guide/" />
					<Resource name="PSVita | Modding" url="https://vita.hacks.guide" />
					<Resource name="PS2 | ROMs desde Samba" url="https://www.vikaskumar.org/2020/10/02/ps2-freemcboot-smb.html" />
				</div>
				<div>
					<p>Recursos</p>
					<Resource name="Batocera Linux" url="https://batocera.org" />
					<Resource name="Servicios que puedes hostear" url="https://awesome-selfhosted.net" />
					<Resource name="Cloudflare Tunnel" url="https://developers.cloudflare.com/cloudflare-one/networks/connectors/cloudflare-tunnel" />
					<Resource name="Mod | Modflared" url="https://modrinth.com/mod/modflared" />
				</div>
			</div>
		</Window>

		<Window title="Credits" app="Markdown">
			<div class="main-container__content__credits">
				<Video
					title="Homebrew Channel WITHOUT Logo!"
					id="eJjDMtsJtng"
				/>
				<Video
					title="Generic 90's TV Music! | George Streicher"
					id="-n-zduNJ0t8"
				/>
				<Video
					title="Every Klonoa Title Screen in Order with Visuals"
					id="o3jeN0tIYQ0"
				/>
			</div>
		</Window>
	</div>
</div>

<style>
	.main-container {
		display:		flex;
		flex-direction:	column;
		gap:			var(--padding-m);
	}

	.main-container__title {
		display:				flex;
		align-items:			center;
		justify-content:		center;

		background-image: 		url("https://i3.ytimg.com/vi/7pCqES0vruY/maxresdefault.jpg");
		background-position:	center;
		background-size:		cover;
		background-repeat:		no-repeat;
		padding:				var(--padding-xl);
	}

	.main-container__title h1 {
		color:				#FFFFFF;
		background-color:	#000000;
		padding:			0 var(--padding-m);
		text-align:			center;
	}

	.main-container__content {
		display:				grid;
		grid-template-columns:	1fr 1fr;
		gap:					var(--padding-m);
	}

	.main-container__content__resources {
		display:		flex;
		flex-wrap:		wrap;
		gap:			var(--padding-m);
	}
	.main-container__content__resources div {
		display:		flex;
		flex-direction:	column;
		gap:			var(--padding-xs);
	}


	.main-container__content__resources p {
		color:	var(--color-window-bg);
		font-size:	smaller;
	}
	.main-container__content__resources p:not(:first-child) {
		margin-top: var(--padding-s);
	}
	.main-container__content__resources p::before {
		content:	"-- ";
	}

	.main-container__content__credits {
		display:		flex;
		flex-direction:	row;
		gap:			var(--padding-m);
	}

	@media screen and (max-width: 728px) {
		.main-container__content {
			display:		flex;
			flex-direction:	column;
		}

		.main-container__content__credits {
			display:		flex;
			flex-direction:	column;
			gap:			var(--padding-m);
		}
	}
</style>