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
	<!-- TODO keywords -->
	<meta
		name="keywords"
		content="hudba, kultura, akce, budějce, české, budějovice, žižkárna, koncerty, trhy, kapely, farmářské, program, workshop, divadlo, party, dj, koncerty, dhogh, muzika, ehmk, brownfield, eventy, industrial, hipster, populární, music, zizkarna, events, actual, popular, live, show, bar, drink, beer, pivo, shots, culture"
	/>
	<meta name="author" content="Vojtěch Divoký" />
	<meta name="viewport" content="width=device-width, initial-scale=1.0" />
</svelte:head>

<div class="px-5">
	<nav class="navbar navbar-expand-lg flex-column align-items-stretch pb-3">
		<!-- TODO galery logo -->
		<div class="d-flex bottom-line mb-3">
			<h1 class="navbar-brand galery-title">galerie nahoře</h1>
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
		<div class="collapse navbar-collapse" id="navbarNavAltMarkup">
			<div class="navbar-nav w-100">
				<a class="nav-item nav-link navbar-button" href="/">aktuální výstava</a>
				<a class="nav-item nav-link navbar-button ms-5" href="/">o galerii</a>
				<a class="nav-item nav-link navbar-button ms-5" href="/">kalendář akcí</a>
				<a class="nav-item nav-link navbar-button ms-5" href="/">kontakt</a>
				<div class="container-fluid"></div>
				<a class="nav-item nav-link navbar-button" href="/">cz</a>
				<!-- TODO slash? -->
				<a class="nav-item nav-link navbar-button" href="/">en</a>
			</div>
		</div>
	</nav>

	<!-- NOTE vertical divider -->
	<!-- <div class="d-none d-md-block border-start border-1 mx-1" /> -->
	<slot />
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

    :global(.bottom-line){
        border-bottom: 1.5px solid var(--black);
    }

    /* TODO unify these font styles across all files */
	:global(.galery-title) {
		font-size: 4.063rem;
		font-weight: 300;
		line-height: 5.184rem;
		letter-spacing: 0em;
		text-transform: uppercase;
	}

	.navbar-button {
		font-size: 1rem;
		font-weight: 500;
		line-height: 1.25rem;
		letter-spacing: 0.05em;
		text-transform: uppercase;
		min-width: fit-content;
	}
</style>
