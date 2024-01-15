<script>
	import DateText from '$lib/DateText.svelte';

	export let title = '';
	export let dateStart = '';
	export let dateEnd = '';
	export let imgPath = '0';
	export let last = false;
</script>

<div class="wrapper px-3" class:border-right={!last}>
	<div class="image-wrapper">
		<div style="background-image: url('/dynamic/thumbnails/{imgPath}.jpg')"></div>
	</div>
	<h3 class="title mt-3">{title}</h3>
	<p class="date"><DateText {dateStart} {dateEnd} /></p>
</div>

<style>
	.wrapper {
		position: relative;
		width: 100%;
		height: 600px;
	}

	.border-right {
		border-right: solid 2px var(--black);
	}

	.image-wrapper {
		width: 100%;
		height: 300px;
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

	.title {
		font-size: 1.875rem;
		font-weight: 300;
		line-height: 2.599rem;
		letter-spacing: 0em;
		text-transform: uppercase;
	}

	.date {
		font-size: 1rem;
		font-weight: 500;
		line-height: 1.556rem;
		letter-spacing: 0.05em;
		
		position: absolute;
		bottom: -1rem;
	}
</style>
