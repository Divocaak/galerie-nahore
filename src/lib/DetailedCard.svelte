<script>
	import DateText from '$lib/DateText.svelte';

	export let title = '';
	export let description = '';
	
	export let author = '';
	export let dateStart = '';
	export let dateEnd = '';
	export let imgPath = '0';

	export let anchorLabel = null;
	export let anchor = null;
</script>

<div class="image-wrapper" id={anchor != null ? anchor : ''}>
	<div style="background-image: url('/dynamic/thumbnails/{imgPath}.jpg')"></div>
</div>
<div class="title-wrapper mt-4 mt-md-5">
	<h3 class="gallery-title">{title}</h3>
	{#if anchorLabel != null}
		<h2 class="anchor-button-date-text anchor-position bottom-line">{anchorLabel}</h2>
	{/if}
</div>
<p class="anchor-button-date-text author-date-text">
	{author}<span>&bull;</span><DateText {dateStart} {dateEnd} />
</p>
<p class="desc mt-5">{description}</p>

<style>
	.image-wrapper {
		width: 100%;
		height: 500px;
	}

	.image-wrapper div {
		position: relative;
		width: 100%;
		height: 100%;
		background-position: 50% 0;
		background-repeat: no-repeat;
		background-size: cover;
		margin: 0 auto;
	}

	.title-wrapper {
		position: relative;
	}

	.title-wrapper h3 {
		max-width: 50%;
	}

	.anchor-position {
		position: absolute;
		right: 0;
		top: 1.5rem;
		width: 30%;
		text-align: right;
	}

	.anchor-button-date-text span {
		margin: 0 1.5rem;
	}

	.desc {
		font-size: 1rem;
		font-weight: 400;
		line-height: 1.875rem;
		letter-spacing: 0em;

		max-width: 50%;
		min-height: 10vh;
	}

	/* sm */
	@media only screen and (max-width: 576px) {
		.desc {
			max-width: 100%;
		}

		.title-wrapper h3 {
			max-width: 100%;
			position: relative;
			top: 1.5rem;
		}

		.anchor-position {
			top: 0rem;
			width: 50%;
		}

		.author-date-text {
			position: relative;
			top: 1.5rem;
		}
	}

	/* md */
	@media only screen and (min-width: 577px) and (max-width: 991px) {
		.desc {
			max-width: 70%;
		}
	}
</style>
