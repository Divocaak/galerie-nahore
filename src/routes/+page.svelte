<script>
	import { lang } from '$lib/stores/LangStore.js';
	import langs from '$lib/localization.json';
	import data from '/dynamic/data.json';
	import DetailedCard from '$lib/DetailedCard.svelte';
	import CalendarCard from '$lib/CalendarCard.svelte';
	import Carousel from 'svelte-light-carousel';
</script>

<DetailedCard
	title={data.actual[$lang + '_title']}
	description={data.actual[$lang + '_description']}
	{...data.actual}
	anchorLabel={langs[$lang].nav.actual}
	anchor={'actual'}
/>
<h2 class="anchor-button-date-text text-end mt-5" id="calendar">{langs[$lang].nav.calendar}</h2>
<div class="calendar top-line bottom-line mb-5 py-3">
	<Carousel slides={data.calendar} dragFree={false} layout={{ xs: 1, sm: 1, md: 2, lg: 3, xl: 4 }}>
		<div slot="slide" let:slide>
			<CalendarCard {...slide} />
		</div>
	</Carousel>
</div>
<DetailedCard
	title={data.about[$lang + '_title']}
	description={data.about[$lang + '_description']}
	{...data.about}
	anchorLabel={langs[$lang].nav.about}
	anchor={'about'}
/>

<style>
	.calendar {
		position: relative;
		width: 100%;
		min-height: 600px;
	}
</style>
