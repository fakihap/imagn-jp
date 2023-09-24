<script>
    import hero_bg from '$lib/images/hero.jpg';
</script>

<div class="hero">
    <div>
        <img id="hero-bg" src={hero_bg} alt="background hero"/>
    </div>
    <div class="hero-headline">
        <div id="headline"><span class="accent">Discover</span> Japan.</div>
        <div>a personal library</div>
    </div>
</div>

<style>
    

	#hero-bg {
		width: 100vw;
		height: 100vh;
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
		letter-spacing: .5rem;
	}

    .accent {
        color: var(--color-theme-1);
    }

</style>