<script>
	import '../app.css';
	import SeaChart from '$lib/components/SeaChart.svelte';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<SeaChart />

<div class="page">
	<Nav />
	<main>
		{@render children()}
	</main>
	<Footer />
</div>
