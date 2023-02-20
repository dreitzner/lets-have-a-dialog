<script>
	import Header from './Header.svelte';
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
	import './styles.css';
</script>

<div class="app">
	<Header />

	<main>
		<section>
			<h1>
				<span class="welcome">
					<picture>
						<source srcset={welcome} type="image/webp" />
						<img src={welcome_fallback} alt="Welcome" />
					</picture>
				</span>
		
				to your new<br />SvelteKit app
			</h1>
		</section>
		<slot />
	</main>

	<footer>
		<p>visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to learn SvelteKit</p>
		<ul>
			<li><a href="/dialog-base">base</a></li>
			<li><a href="/dialog-show">show</a></li>
			<li><a href="/dialog-click-outside">click-outside</a></li>
			<li><a href="/dialog-on-close">on-close</a></li>
			<li><a href="/dialog-style">style</a></li>
			<li><a href="/dialog-transition">transition</a></li>
			<li><a href="/dialog-transition-css">transition-css</a></li>
		</ul>
	</footer>
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 64rem;
		margin: 0 auto;
		box-sizing: border-box;
	}
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
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

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 12px;
	}

	footer a {
		font-weight: bold;
	}

	ul {
		margin: 0;
		padding: 0;
		display: flex;
		list-style: none;
		gap: 15px
	}


	@media (min-width: 480px) {
		footer {
			padding: 12px 0;
		}
	}
</style>
