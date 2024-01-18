<script>
	import { lang } from '$lib/stores/LangStore.js';
	import langs from '$lib/localization.json';
</script>

<svelte:head>
	<link
		rel="stylesheet"
		href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.10.3/font/bootstrap-icons.css"
	/>
	<link
		href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/css/bootstrap.min.css"
		rel="stylesheet"
		integrity="sha384-aFq/bzH65dt+w6FI2ooMVUpc+21e0SRygnTpmBvdBgSdnuTN7QbdgL+OapgHtvPp"
		crossorigin="anonymous"
	/>
	<script
		src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha2/dist/js/bootstrap.bundle.min.js"
		integrity="sha384-qKXV1j0HvMUeCBQ+QVp7JcfGl760yU08IQ+GpUo5hlbpg51QRiuqHAJz8+BrxE/N"
		crossorigin="anonymous"
	></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
	<meta charset="windows-1250" />
	<!-- TODO keywords -->
	<meta name="keywords" content="" />
	<meta name="author" content="Vojtěch Divoký" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<div class="px-md-5 px-3">
	<nav class="navbar navbar-expand-lg flex-column align-items-stretch pb-3">
		<!-- TODO galery logo -->
		<div class="d-flex justify-content-between bottom-line mb-3">
			<h1 class="gallery-title">galerie nahoře</h1>
			<button
				class="navbar-toggler"
				type="button"
				data-bs-toggle="collapse"
				data-bs-target="#navbarNavAltMarkup"
				aria-controls="navbarNavAltMarkup"
				aria-expanded="false"
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon" />
			</button>
		</div>
		<div class="collapse navbar-collapse pb-2 pm-lg-0" id="navbarNavAltMarkup">
			<div class="navbar-nav w-100">
				<a class="nav-item nav-link navbar-button anchor-button-date-text" href="/#actual">
					{langs[$lang].nav.actual}
				</a>
				<a class="nav-item nav-link navbar-button anchor-button-date-text ms-lg-5" href="/#about">
					{langs[$lang].nav.about}
				</a>
				<a
					class="nav-item nav-link navbar-button anchor-button-date-text ms-lg-5"
					href="/#calendar"
				>
					{langs[$lang].nav.calendar}
				</a>
				<a class="nav-item nav-link navbar-button anchor-button-date-text ms-lg-5" href="/#contact">
					{langs[$lang].nav.contact}
				</a>
				<div class="container-fluid d-none d-lg-block"></div>
				<div class="nav-item nav-link navbar-button anchor-button-date-text">
					<a href="/" on:click={() => lang.set('cs')}>cz</a>
					&nbsp;&sol;&nbsp;
					<a href="/" on:click={() => lang.set('en')}>en</a>
				</div>
			</div>
		</div>
	</nav>
	<slot />
	<footer class="row text-center my-5 py-5 top-line" id="contact">
		<div class="col-12 col-md-4">
			<h3 class="footer-col-name">{langs[$lang].footer[0].title}</h3>
			<p class="footer-content">
				{langs[$lang].footer[0].line}<br />{langs[$lang].footer[0].secondLine}
			</p>
		</div>
		<div class="col-12 col-md-4 mt-5 mt-md-0">
			<h3 class="footer-col-name">{langs[$lang].footer[1].title}</h3>
			<p class="footer-content">
				{langs[$lang].footer[1].line}<br />{langs[$lang].footer[1].secondLine}
			</p>
		</div>
		<div class="col-12 col-md-4 mt-5 mt-md-0">
			<h3 class="footer-col-name">{langs[$lang].footer[2].title}</h3>
			<p class="footer-content">
				{langs[$lang].footer[2].line}<br />{langs[$lang].footer[2].secondLine}
			</p>
		</div>
	</footer>
</div>

<style lang="scss">
	:root {
		--black: #222222;
		--white: white;
	}

	@font-face {
		font-family: 'SpaceGrotesk';
		src: url('/SpaceGrotesk-VariableFont_wght.ttf');
	}

	:global(html) {
		scroll-behavior: smooth;
		overflow-x: hidden;
	}

	:global(p, h1, h2, h3, h4, h5, h6, a) {
		font-family: 'SpaceGrotesk', 'Courier New', monospace;
		color: var(--black) !important;
	}

	:global(.bottom-line) {
		border-bottom: 1.5px solid var(--black);
	}

	:global(.top-line) {
		border-top: 1.5px solid var(--black);
	}

	:global(.gallery-title) {
		font-size: 4.063rem;
		font-weight: 300;
		line-height: 5.184rem;
		letter-spacing: 0em;
		text-transform: uppercase;
	}

	:global(.anchor-button-date-text) {
		font-size: 1rem;
		font-weight: 500;
		line-height: 1.25rem;
		letter-spacing: 0.05em;
		text-transform: uppercase;
	}

	.navbar-button a {
		text-decoration: none;
	}

	.navbar-button {
		min-width: fit-content;
	}

	.footer-col-name {
		font-size: 1rem;
		font-weight: 400;
		line-height: 1.276rem;
		letter-spacing: 0em;
	}

	.footer-content {
		font-size: 1rem;
		font-weight: 400;
		line-height: 1.865rem;
		letter-spacing: 0em;
		color: #000000 !important;
	}

	.navbar-toggler {
		width: min-content;
		height: min-content;
		border-radius: 0;
		border: none;
	}

	.navbar-toggler:focus {
		box-shadow: none;
	}

	/* sm */
	@media only screen and (max-width: 576px) {
		:global(.gallery-title) {
			font-size: 3.063rem;
			line-height: 4.184rem;
		}
	}

	/* sm to md */
	@media only screen and (max-width: 991px) {
		.navbar-button:not(div) {
			border-bottom: 0.5px solid var(--black);
		}

		.navbar-collapse {
			border-bottom: 1.5px solid var(--black);
		}
	}
</style>
