<script>
	// import Counter from './Counter.svelte';
	// import welcome from '$lib/images/svelte-welcome.webp';
	// import welcome_fallback from '$lib/images/svelte-welcome.png';
	import hero_bg from '$lib/images/hero.jpg';

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<hero>
		<img id="hero-bg" src={hero_bg} alt="background hero"/>
	</hero>
	<div class="hero-headline">
		<div id="headline">Nature speaks.</div>
		<div>a personal library</div>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
		
		position: absolute;
		top: 0;
		left: 0px;

		z-index: -10;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	hero {
		width: 100vw;
		height: 100vh;
	}

	#hero-bg {
		width: 100%;
		height: 100%;
		object-fit: cover;

		/* object-position: 0 0rem; */
	}

	.hero-headline {
		position: absolute;
		top: 65vh;
		left: 15vw;
		color: var(--color-text-white);
		text-shadow: black 0px 2px 10px;
		font-size: 1.4rem;
	}

	.hero-headline #headline {
		font-size: var(--font-size-headline);
		letter-spacing: .8rem;
	}

</style>
