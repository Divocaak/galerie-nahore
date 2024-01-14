<script>
	export let title = '';
	export let author = '';
	export let dateStart = '';
	export let dateEnd = '';
	export let desc = '';
	export let imgPath = '0';
	export let anchorLabel = null;
	export let anchor = null;
</script>

<div class="image-wrapper">
	<div style="background-image: url('/dynamic/thumbnails/{imgPath}.jpg')"></div>
</div>
<div class="title-wrapper mt-5">
	<h2 class="galery-title">{title}</h2>
	{#if anchorLabel != null}
		<p class="anchor bottom-line">{anchorLabel}</p>
        <!-- TODO anchors clickable -->
	{/if}
</div>
TODO dates
<p class="author-date-text">{author}<span>&bull;</span>22. 4.&nbsp;&ndash;&nbsp;17. 8. 2023</p>
<p class="desc mt-5">{desc}</p>

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

	.anchor {
		font-size: 1rem;
		font-weight: 500;
		line-height: 1.25rem;
		letter-spacing: 0.05em;
		text-transform: uppercase;

		position: absolute;
		right: 0;
		top: 1.5rem;
		width: 30%;
		text-align: right;
	}

	.author-date-text {
		font-size: 1rem;
		font-weight: 500;
		line-height: 1.25rem;
		letter-spacing: 0.05em;
		text-transform: uppercase;
	}

	.author-date-text span {
		margin: 0 1.5rem;
	}

	.desc {
		font-size: 1rem;
		font-weight: 400;
		line-height: 1.875rem;
		letter-spacing: 0em;

		max-width: 50%;
	}
</style>
