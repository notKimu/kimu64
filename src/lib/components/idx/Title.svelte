<script lang="ts">
	interface props {
		text: string;
	};

	let props: props = $props();

	const dur = 1; 
	const len = dur * props.text.length;
</script>

<div class="container">
	<p class="text">
		{#each props.text as char, i}
				<span class="text__letter" style="--d:{i * dur}s; z-index: {len - i};">
					{char}
				</span>
		{/each}
	</p>
</div>

<style>
  .text {
    color:			#fff;
    letter-spacing:	-10px;
    text-shadow:	0 0 3px #60385c,
      				0 1px 0 #60385c,
      				0 2px 0 #60385c,
      				0 3px 0 #60385c,
      				0 4px 0 #60385c,
      				0 5px 0 #60385c,
      				0 6px 0 #60385c,
      				0 7px 0 #60385c,
      				0 8px 0 #60385c,
      				0 9px 0 #60385c,
      				0 10px 0 #60385c,
      				0 11px 0 #60385c,
      				0 12px 0 #60385c,
      				0 13px 0 #60385c,
      				0 14px 0 #60385c,
      				0 15px 0 #60385c;
  }

  .text__letter {
    position:				relative;
    font-size:				clamp(1rem, 20vw, 5rem);
	display:				inline-block;
    font-family:			"Super Mario";
    -webkit-text-stroke:	0.25rem #60385c;
    animation:				boing 8s infinite;
    animation-delay:		var(--d);
  }

  @keyframes boing {
    0% {
      transform:	translateY(0px);
    }
	6.25% {
		transform:	translateY(-4px);
	}
	12.5% {
		transform:	translateY(0px);
	}
    100% {
      transform:	translateY(0px);
    }
  }

  @media screen and (max-width: 728px) {
	.text__letter {
		font-size: 4rem
	}
  }

  @media screen and (max-width: 450px) {
	.text {
		letter-spacing:	-6px;
	}
	.text__letter {
		font-size:				3rem;
  		-webkit-text-stroke:	0.15rem #60385c;
	}
  }
</style>
