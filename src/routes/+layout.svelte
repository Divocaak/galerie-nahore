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

	<meta charset="windows-1250" />
	<meta
		name="keywords"
		content="hudba, kultura, akce, budějce, české, budějovice, žižkárna, koncerty, trhy, kapely, farmářské, program, workshop, divadlo, party, dj, koncerty, dhogh, muzika, ehmk, brownfield, eventy, industrial, hipster, populární, music, zizkarna, events, actual, popular, live, show, bar, drink, beer, pivo, shots, culture"
	/>
	<meta name="author" content="Vojtěch Divoký" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<nav class="navbar navbar-expand-lg sticky-top">
	<h1 class="navbar-brand text-uppercase fw-bold display-1">galerie nahoře</h1>
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
	<div class="collapse navbar-collapse" id="navbarNavAltMarkup">
		<div class="pe-5 navbar-nav ms-auto">
			<a class="nav-item nav-link text-uppercase" href="/">aktuální výstava</a>
			<a class="nav-item nav-link text-uppercase" href="/">o galerii</a>
			<a class="nav-item nav-link text-uppercase" href="/">kalendář akcí</a>
			<a class="nav-item nav-link text-uppercase" href="/">kontakt</a>
			<!-- <div class="d-none d-md-block border-start border-1 mx-1" /> -->
		</div>
	</div>
</nav>

<slot />

<style lang="scss">
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
	}

	:global();
</style>
