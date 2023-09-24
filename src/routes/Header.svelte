<script>
	import { page } from '$app/stores';
	import './styles.css';
	import logo from '$lib/images/imagn.jp.png';
	import github from '$lib/images/github.svg';
  	// import { onMount } from 'svelte';

// 	/**
//    * @type {number | undefined}
//    */
// 	let windowYScrollAmount;
// 	onMount(() => {
// 		const window = document.querySelector('window');
// 		windowYScrollAmount = document.
// 	})
</script>

<header>
	<div class="logo">
		<a href="/">
			<img src={logo} alt="nature.me" />
		</a>
	</div>

	<nav>
		
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Home</a>
			</li>	
			<li aria-current={$page.url.pathname.startsWith('/library') ? 'page' : undefined}>
				<a href="/library">Library</a>
			</li>
			<li aria-current={$page.url.pathname === '/gear' ? 'page' : undefined}>
				<a href="/gear">Gear</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">About</a>
			</li>
		</ul>
		
	</nav>

	<!-- <div class="corner">
		<a href="https://github.com/sveltejs/kit">
			<img src={github} alt="GitHub" />
		</a>
	</div> -->
</header>

<style>
	header {
		position:fixed;
		top: 0px;

		display: flex;
		justify-content: space-between;
		align-items: center;
		
		width: 100svw;
		height: var(--nav-height);
		padding: 0 10rem;

		/* background-color: #eeeeee; */

		backdrop-filter: blur(2px);
		box-shadow: 0 2px 10px rgb(0 0 0 / 10%), 0 10px 15px rgb(0 0 0 / 20%);
		box-sizing: border-box;
		background-image: linear-gradient(45deg, rgba(255,255,255,0), rgba(255,255,255,0));
		mix-blend-mode: hard-light;
	}

	.logo {
		width: 10rem;
	}	

	.logo a img {
		width: 100%;
	}

	nav {
		display: flex;
		justify-content: center;
		width: 40rem;
	}

	ul {
		width: 100%;
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: space-around;
		align-items: center;
		list-style: none;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 3px;
		--width-prc: 80%;
		content: '';
		width: var(--width-prc);
		height: var(--size);
		background: var(--color-theme-1);
		position: absolute;
		top: 0;
		left: calc((100% - var(--width-prc)) / 2);	
	}

	li::before {
		--size: 3px;
		content: '';
		width: 0;
		height: var(--size);
		background: var(--color-theme-1);
		position: absolute;
		top: .4rem;
		

		transition: .3s;
	}

	li:hover::before {
		--width-prc: 80%;
		width: var(--width-prc);
		left: calc((100% - var(--width-prc)) / 2);	
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 0.5rem;
		color: var(--color-text-white);
		font-weight: 300;
		font-size: var(--font-size-navitem);
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	nav a:hover {
		font-weight: 500;
		color: var(--color-theme-1);
	}
</style>
