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

        <div class="more">
            <a href="/#hook">Learn More</a>
        </div>
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

        transition: 0.3s;
    }

    .accent:hover {
        text-shadow: var(--color-theme-1) 0 0 20px;
        letter-spacing: .6rem;
    }

    .more {
        background-color: var(--color-theme-1);
        border-radius: 30px;

        width: max-content;
        height: max-content;

        padding: .5rem .8rem;
        margin: 1.3rem 1rem;

        text-decoration: none;
        font-size: 1.6rem;
        
        box-shadow: black 0 0 10px;
    }

    .more:hover {
        box-shadow: var(--color-theme-1) 0 0 20px;
    }

    .more a {
        color: white;
        text-decoration: none;
    }

</style>