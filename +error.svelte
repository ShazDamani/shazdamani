<script>
	import { page } from '$app/state';
</script>

<svelte:head>
	<title>uncharted waters · shaz damani</title>
</svelte:head>

<article class="uncharted">
	<p class="eyebrow">{page.status}</p>
	<h1>uncharted waters</h1>
	<div class="prose">
		<p>
			This page isn't on the chart. It may have drifted, it may have sunk, it may never have
			existed at all. The sea keeps its own records.
		</p>
		<p><a href="/">return to the surface →</a></p>
	</div>
</article>

<style>
	.uncharted {
		text-align: center;
		padding: 3rem 0;
	}

	h1 {
		margin: 0 0 1rem;
	}
</style>
