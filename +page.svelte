<script>
	import { posts, prettyDate } from '$lib/posts.js';

	const moods = [
		'cautiously victorious',
		'seaworthy',
		'plotting (benevolently)',
		'gothic but hydrated',
		'unbothered at depth'
	];

	const tunes = [
		'whale song (allegedly)',
		'sonar pings, lo-fi',
		'sea shanties, ironically at first',
		'the hum of the bilge pump',
		'something with a harpsichord'
	];

	const day = Math.floor(Date.now() / 86400000);
	const mood = moods[day % moods.length];
	const tune = tunes[day % tunes.length];

	const today = new Date()
		.toLocaleDateString('en-US', { weekday: 'long', month: 'long', day: 'numeric' })
		.toLowerCase();

	const recent = posts.slice(0, 3);
</script>

<svelte:head>
	<title>shaz damani · dispatches from the deep end</title>
	<meta name="description" content="The personal site of Shaz Damani: public health, travel, baking, sharks, and one novel in progress." />
</svelte:head>

<article class="entry">
	<p class="eyebrow">{today}</p>
	<p class="meta moodline">mood: {mood} · listening to: {tune} · location: sea level, nyc</p>

	<h1>so. a website.</h1>

	<div class="prose">
		<p>
			I've been threatening to make one of these for years, and apparently all it took was one
			long weekend and a mild vendetta. Welcome.
		</p>
		<p>
			The short version: I run public health programs for a living, which mostly means strategy,
			spreadsheets, and a volume of email that would frighten you. Everything else, the travel,
			the baking, the novel I am absolutely writing and not just thinking about in the shower,
			lives here now. One place. Like a respectable hoarder.
		</p>
		<p>
			Look around. Mind the jellyfish. The <a href="/guestbook">guestbook</a> is real and I will
			read it.
		</p>
	</div>
</article>

<hr class="rule" />

<section aria-label="recent dispatches">
	<p class="eyebrow">recent dispatches</p>
	<ul class="dispatch-list">
		{#each recent as post (post.slug)}
			<li>
				<a href="/sidequests/{post.slug}">{post.title}</a>
				<span class="meta">· {prettyDate(post.date)}</span>
			</li>
		{/each}
	</ul>
	<p class="all-link"><a href="/sidequests">see the full chart →</a></p>
</section>

<style>
	.moodline {
		margin: 0 0 1.25rem;
	}

	h1 {
		margin: 0 0 0.9rem;
	}

	.dispatch-list {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.dispatch-list li {
		margin-bottom: 0.55rem;
	}

	.dispatch-list a {
		font-family: var(--serif);
		font-size: 1.02rem;
		text-decoration: none;
	}

	.dispatch-list a:hover {
		text-decoration: underline;
	}

	.all-link {
		margin-top: 1rem;
	}

	.all-link a {
		font-family: var(--mono);
		font-size: 0.75rem;
		letter-spacing: 0.08em;
		text-decoration: none;
	}
</style>
