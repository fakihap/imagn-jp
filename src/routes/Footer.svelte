<script>
    import github from '$lib/images/github.svg';
</script>


<footer>
    <div>Made with love | 2023</div>
    <div class="shield">
        <a href="https://github.com/fakihap/imagn-jp">
            <img src={github} alt="GitHub" />
        </a>
    </div>
</footer>

<style>
    footer {
        background-color: var(--color-theme-2);

       
		position: absolute;
		top: 500vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;

		height: 4rem;
        width: 100vw;
	}

    .shield {
        height: 3rem;
        width: 100vw;

        display: flex;
        justify-content: center;
        align-items: center;
    }

    .shield a img {
        height: 3rem;
    }

	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>