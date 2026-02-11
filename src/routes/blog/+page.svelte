<script lang="ts">
	import RevealOnScroll from '$lib/components/RevealOnScroll.svelte';

	const posts = [
		{
			title: '5 Landscape Trends Transforming Outdoor Living in 2026',
			excerpt: 'From climate-adaptive plantings to multi-functional spaces, here are the top trends we\'re seeing in residential landscape design this year.',
			date: 'February 5, 2026',
			category: 'Trends',
			readTime: '5 min read'
		},
		{
			title: 'The Complete Guide to Choosing Patio Materials',
			excerpt: 'Natural stone, pavers, stamped concrete, or composite? We break down the pros, cons, and costs of every popular patio material.',
			date: 'January 22, 2026',
			category: 'Guides',
			readTime: '8 min read'
		},
		{
			title: 'How Proper Drainage Saves Your Foundation',
			excerpt: 'Poor drainage doesn\'t just ruin your lawn. It can cause serious structural damage. Here\'s what every homeowner should know.',
			date: 'January 10, 2026',
			category: 'Education',
			readTime: '4 min read'
		},
		{
			title: 'Before & After: A Hillside Transformation',
			excerpt: 'See how we turned a steep, unusable slope into a stunning terraced garden with retaining walls and native plantings.',
			date: 'December 18, 2025',
			category: 'Projects',
			readTime: '3 min read'
		},
		{
			title: 'Outdoor Lighting: More Than Just Aesthetics',
			excerpt: 'Quality landscape lighting enhances safety, security, and property value. Here\'s our approach to designing the perfect lighting scheme.',
			date: 'December 5, 2025',
			category: 'Education',
			readTime: '6 min read'
		},
		{
			title: 'Winter Prep: Protecting Your Landscape Investment',
			excerpt: 'The steps you take before winter directly impact how your landscape looks in spring. Our seasonal checklist for homeowners.',
			date: 'November 15, 2025',
			category: 'Guides',
			readTime: '5 min read'
		}
	];
</script>

<svelte:head>
	<title>Blog | Good To Go Contracting</title>
</svelte:head>

<!-- Hero -->
<section class="relative flex min-h-[50vh] items-center overflow-hidden bg-black">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="absolute top-0 right-0 h-full w-1/3 bg-amber/[0.03]" style="clip-path: polygon(40% 0, 100% 0, 100% 100%, 0% 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 py-32 lg:px-8">
		<div class="max-w-2xl">
			<span class="font-display text-sm tracking-[0.2em] text-amber">INSIGHTS & IDEAS</span>
			<h1 class="animate-fade-up mt-4 font-display text-5xl tracking-wide text-white lg:text-7xl">
				THE GOOD TO GO BLOG
			</h1>
			<p class="animate-fade-up mt-6 text-lg text-zinc" style="animation-delay: 100ms">
				Tips, trends, and behind-the-scenes looks at our landscape and hardscape projects.
			</p>
		</div>
	</div>
</section>

<!-- Blog Grid -->
<section class="bg-obsidian py-20 lg:py-28">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<!-- Featured Post -->
		<RevealOnScroll>
			<a href="/blog" class="group block overflow-hidden border border-white/5 bg-carbon transition-all hover:border-amber/20">
				<div class="grid lg:grid-cols-2">
					<div class="aspect-[16/10] bg-graphite lg:aspect-auto">
						<div class="flex h-full items-center justify-center text-zinc/20">
							<div class="text-center">
								<svg class="mx-auto h-16 w-16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
								<p class="mt-2 text-sm">Featured Post Image</p>
							</div>
						</div>
					</div>
					<div class="flex flex-col justify-center p-8 lg:p-12">
						<div class="flex items-center gap-3">
							<span class="border border-amber/30 bg-amber/10 px-3 py-1 text-[10px] font-semibold uppercase tracking-wider text-amber">{posts[0].category}</span>
							<span class="text-xs text-zinc">{posts[0].date}</span>
						</div>
						<h2 class="mt-4 font-display text-2xl tracking-wide text-white transition-colors group-hover:text-amber lg:text-3xl">{posts[0].title.toUpperCase()}</h2>
						<p class="mt-3 leading-relaxed text-zinc">{posts[0].excerpt}</p>
						<div class="mt-6 flex items-center gap-2 text-sm font-medium text-zinc transition-colors group-hover:text-amber">
							Read Article
							<svg class="h-4 w-4 transition-transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7" /></svg>
						</div>
					</div>
				</div>
			</a>
		</RevealOnScroll>

		<!-- Post Grid -->
		<div class="stagger mt-10 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
			{#each posts.slice(1) as post, i}
				<RevealOnScroll delay={i * 60}>
					<a href="/blog" class="group block overflow-hidden border border-white/5 bg-carbon transition-all hover:border-amber/20">
						<div class="aspect-[16/10] bg-graphite">
							<div class="flex h-full items-center justify-center text-zinc/20">
								<div class="text-center">
									<svg class="mx-auto h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
									<p class="mt-1 text-xs">Post Image</p>
								</div>
							</div>
						</div>
						<div class="p-6">
							<div class="flex items-center gap-3">
								<span class="border border-amber/30 bg-amber/10 px-2.5 py-0.5 text-[10px] font-semibold uppercase tracking-wider text-amber">{post.category}</span>
								<span class="text-xs text-zinc/60">{post.readTime}</span>
							</div>
							<h3 class="mt-3 font-display text-lg tracking-wide text-white transition-colors group-hover:text-amber">{post.title.toUpperCase()}</h3>
							<p class="mt-2 text-sm leading-relaxed text-zinc line-clamp-2">{post.excerpt}</p>
							<div class="mt-4 text-xs text-zinc/60">{post.date}</div>
						</div>
					</a>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>
