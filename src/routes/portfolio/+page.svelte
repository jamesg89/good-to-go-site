<script lang="ts">
	import RevealOnScroll from '$lib/components/RevealOnScroll.svelte';

	const categories = ['All', 'Landscape Design', 'Installation', 'Lighting', 'Concrete', 'Earthworks'];
	let activeCategory = $state('All');

	const projects = [
		{ title: 'Modern Patio & Outdoor Kitchen', category: 'Installation', description: 'Complete outdoor living area with stamped concrete patio, built-in grill station, and custom seating.' },
		{ title: 'Hillside Terraced Garden', category: 'Landscape Design', description: 'Multi-level garden design with native plantings, stone retaining walls, and water feature.' },
		{ title: 'Estate Landscape Lighting', category: 'Lighting', description: 'Full property architectural and landscape lighting design with smart controls.' },
		{ title: 'Decorative Stamped Concrete', category: 'Concrete', description: 'Custom stamped and stained concrete driveway and walkway installation.' },
		{ title: 'Backyard Drainage Solution', category: 'Earthworks', description: 'French drain system with decorative rain garden and regraded lawn.' },
		{ title: 'Contemporary Front Yard', category: 'Landscape Design', description: 'Low-maintenance modern landscape with ornamental grasses and boulder accents.' },
		{ title: 'Pergola & Fire Pit Area', category: 'Installation', description: 'Cedar pergola with string lighting, natural stone fire pit, and flagstone patio.' },
		{ title: 'Garden Path Uplighting', category: 'Lighting', description: 'Subtle pathway and garden accent lighting creating dramatic evening atmosphere.' },
		{ title: 'Custom Retaining Wall', category: 'Concrete', description: 'Engineered segmental retaining wall with integrated planting pockets.' },
		{ title: 'Property Grading Project', category: 'Earthworks', description: 'Full property regrading to resolve water runoff issues and create usable lawn space.' },
		{ title: 'Japanese-Inspired Garden', category: 'Landscape Design', description: 'Zen garden design with raked gravel, specimen maples, and stone lanterns.' },
		{ title: 'Pool Deck Renovation', category: 'Installation', description: 'Travertine pool deck replacement with integrated lighting and new plantings.' },
	];

	let filteredProjects = $derived(
		activeCategory === 'All'
			? projects
			: projects.filter((p) => p.category === activeCategory)
	);
</script>

<svelte:head>
	<title>Portfolio | Good To Go Contracting</title>
</svelte:head>

<!-- Hero -->
<section class="relative flex min-h-[50vh] items-center overflow-hidden bg-black">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="absolute top-0 right-0 h-full w-1/3 bg-amber/[0.03]" style="clip-path: polygon(40% 0, 100% 0, 100% 100%, 0% 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 py-32 lg:px-8">
		<div class="max-w-2xl">
			<span class="font-display text-sm tracking-[0.2em] text-amber">OUR WORK</span>
			<h1 class="animate-fade-up mt-4 font-display text-5xl tracking-wide text-white lg:text-7xl">
				THE GOOD TO GO PORTFOLIO
			</h1>
			<p class="animate-fade-up mt-6 text-lg text-zinc" style="animation-delay: 100ms">
				Browse our collection of completed projects and see the quality and craftsmanship
				we bring to every landscape and hardscape installation.
			</p>
		</div>
	</div>
</section>

<!-- Filter & Grid -->
<section class="bg-obsidian py-20 lg:py-28">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<!-- Category Filter -->
		<RevealOnScroll>
			<div class="flex flex-wrap justify-center gap-2">
				{#each categories as category}
					<button
						class="px-5 py-2 text-sm font-medium transition-all {activeCategory === category
							? 'bg-amber text-black'
							: 'border border-white/10 bg-white/5 text-zinc hover:border-amber/30 hover:text-white'}"
						onclick={() => (activeCategory = category)}
					>
						{category}
					</button>
				{/each}
			</div>
		</RevealOnScroll>

		<!-- Project Grid -->
		<div class="mt-12 grid gap-3 sm:grid-cols-2 lg:grid-cols-3">
			{#each filteredProjects as project, i (project.title)}
				<div class="img-zoom group">
					<div class="relative aspect-[4/3] overflow-hidden border border-white/5 bg-graphite">
						<div class="flex h-full items-center justify-center text-zinc/20">
							<div class="text-center">
								<svg class="mx-auto h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
								<p class="mt-2 text-xs">{project.title}</p>
							</div>
						</div>
						<!-- Overlay -->
						<div class="absolute inset-0 flex items-end bg-gradient-to-t from-black/90 via-black/30 to-transparent p-6 opacity-0 transition-opacity duration-300 group-hover:opacity-100">
							<div>
								<span class="text-[10px] font-semibold uppercase tracking-[0.15em] text-amber">{project.category}</span>
								<h3 class="mt-1 font-display text-lg tracking-wide text-white">{project.title.toUpperCase()}</h3>
								<p class="mt-1 text-sm text-ash">{project.description}</p>
							</div>
						</div>
					</div>
				</div>
			{/each}
		</div>

		{#if filteredProjects.length === 0}
			<div class="py-20 text-center">
				<p class="text-zinc">No projects found in this category yet.</p>
			</div>
		{/if}
	</div>
</section>

<!-- CTA -->
<section class="relative overflow-hidden bg-black py-24">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="relative mx-auto max-w-4xl px-6 text-center lg:px-8">
		<RevealOnScroll>
			<h2 class="font-display text-5xl tracking-wide text-white lg:text-6xl">
				READY TO GET STARTED?
			</h2>
			<p class="mx-auto mt-6 max-w-xl text-lg text-zinc">
				Your dream outdoor space is just a conversation away. Let's make it happen.
			</p>
			<a
				href="/contact"
				class="mt-10 inline-flex items-center gap-2 bg-amber px-8 py-4 text-sm font-bold uppercase tracking-wider text-black transition-all hover:bg-gold"
			>
				Start Your Project
			</a>
		</RevealOnScroll>
	</div>
</section>
