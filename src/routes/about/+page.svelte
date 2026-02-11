<script lang="ts">
	import RevealOnScroll from '$lib/components/RevealOnScroll.svelte';

	const values = [
		{
			title: 'Quality Craftsmanship',
			description:
				'Every stone, plank, and plant is placed with precision. We never cut corners because your outdoor space deserves the same care as your home.',
			icon: 'quality'
		},
		{
			title: 'Transparent Process',
			description:
				'From detailed proposals to regular progress updates, you always know exactly where your project stands and what to expect next.',
			icon: 'process'
		},
		{
			title: 'In-House Expertise',
			description:
				'Our team handles design, installation, and project management internally. No subcontractor guesswork, just seamless execution.',
			icon: 'team'
		},
		{
			title: 'Lasting Results',
			description:
				'We build with premium materials and time-tested techniques. Our work is designed to look beautiful and perform flawlessly for years.',
			icon: 'lasting'
		}
	];

	const team = [
		{ name: 'Owner / Lead Designer', role: 'Founder & Principal Designer' },
		{ name: 'Project Manager', role: 'Operations & Client Relations' },
		{ name: 'Lead Installer', role: 'Hardscape & Landscape Specialist' }
	];
</script>

<svelte:head>
	<title>About | Good To Go Contracting</title>
</svelte:head>

<!-- Hero -->
<section class="relative flex min-h-[60vh] items-center overflow-hidden bg-black">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="absolute top-0 right-0 h-full w-1/3 bg-amber/[0.03]" style="clip-path: polygon(40% 0, 100% 0, 100% 100%, 0% 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 py-32 lg:px-8">
		<div class="max-w-2xl">
			<span class="font-display text-sm tracking-[0.2em] text-amber">ABOUT US</span>
			<h1 class="animate-fade-up mt-4 font-display text-5xl tracking-wide text-white lg:text-7xl">
				BUILT ON PASSION,<br />DRIVEN BY CRAFT
			</h1>
			<p class="animate-fade-up mt-6 text-lg text-zinc" style="animation-delay: 100ms">
				We're not just contractors. We're designers, builders, and problem-solvers who
				genuinely love transforming outdoor spaces.
			</p>
		</div>
	</div>
</section>

<!-- Story -->
<section class="bg-obsidian py-28 lg:py-36">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="grid items-center gap-16 lg:grid-cols-2">
			<RevealOnScroll>
				<div class="relative">
					<div class="aspect-[4/3] overflow-hidden border border-white/10 bg-graphite">
						<div class="flex h-full items-center justify-center text-zinc/30">
							<div class="text-center">
								<svg class="mx-auto h-16 w-16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
								<p class="mt-2 text-sm">Company / Team Photo</p>
							</div>
						</div>
					</div>
					<div class="absolute -right-3 -bottom-3 h-16 w-16 border-r-2 border-b-2 border-amber/40"></div>
					<div class="absolute -top-3 -left-3 h-16 w-16 border-t-2 border-l-2 border-amber/40"></div>
				</div>
			</RevealOnScroll>

			<RevealOnScroll delay={100}>
				<div>
					<span class="font-display text-sm tracking-[0.2em] text-amber">OUR STORY</span>
					<h2 class="mt-2 font-display text-4xl tracking-wide text-white lg:text-5xl">
						FROM HUMBLE BEGINNINGS TO PREMIUM LANDSCAPES
					</h2>
					<div class="mt-4 h-px w-20 bg-amber"></div>
					<p class="mt-6 leading-relaxed text-ash">
						Good To Go Contracting started with a simple pickup truck, a passion for the
						outdoors, and a commitment to doing things right. What began as a small landscaping
						operation has grown into a full-service landscape design and construction firm
						trusted by homeowners across the region.
					</p>
					<p class="mt-4 leading-relaxed text-zinc">
						Over the years, we've expanded our capabilities to include everything from
						landscape design and installation to outdoor lighting, carpentry, concrete work,
						earthworks, and seasonal snow management. But our core philosophy has never changed:
						treat every project like it's our own property.
					</p>
					<p class="mt-4 leading-relaxed text-zinc">
						Today, our team brings together experienced designers, skilled tradespeople, and
						dedicated project managers who share a common goal: delivering outdoor spaces that
						exceed expectations and stand the test of time.
					</p>
				</div>
			</RevealOnScroll>
		</div>
	</div>
</section>

<!-- Values -->
<section class="bg-carbon py-28 lg:py-36">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="text-center">
				<span class="font-display text-sm tracking-[0.2em] text-amber">OUR VALUES</span>
				<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">
					WHAT SETS US APART
				</h2>
			</div>
		</RevealOnScroll>

		<div class="stagger mt-16 grid gap-5 sm:grid-cols-2">
			{#each values as value, i}
				<RevealOnScroll delay={i * 80}>
					<div class="flex gap-6 border border-white/5 bg-obsidian p-8">
						<div class="flex h-10 w-10 shrink-0 items-center justify-center border border-amber/30 bg-amber/10">
							{#if value.icon === 'quality'}
								<svg class="h-5 w-5 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" /></svg>
							{:else if value.icon === 'process'}
								<svg class="h-5 w-5 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4" /></svg>
							{:else if value.icon === 'team'}
								<svg class="h-5 w-5 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2" /><circle cx="9" cy="7" r="4" /><path d="M23 21v-2a4 4 0 00-3-3.87m-4-12a4 4 0 010 7.75" /></svg>
							{:else if value.icon === 'lasting'}
								<svg class="h-5 w-5 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" /></svg>
							{/if}
						</div>
						<div>
							<h3 class="font-display text-xl tracking-wide text-white">{value.title.toUpperCase()}</h3>
							<p class="mt-2 text-sm leading-relaxed text-zinc">{value.description}</p>
						</div>
					</div>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- Team -->
<section class="bg-obsidian py-28 lg:py-36">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="text-center">
				<span class="font-display text-sm tracking-[0.2em] text-amber">OUR TEAM</span>
				<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">THE PEOPLE BEHIND THE WORK</h2>
				<p class="mx-auto mt-4 max-w-2xl text-zinc">
					Our skilled team brings together decades of combined experience in landscape design,
					construction, and project management.
				</p>
			</div>
		</RevealOnScroll>

		<div class="stagger mt-16 grid gap-6 sm:grid-cols-3">
			{#each team as member, i}
				<RevealOnScroll delay={i * 80}>
					<div class="group text-center">
						<div class="mx-auto aspect-square w-full max-w-[280px] overflow-hidden border border-white/5 bg-graphite">
							<div class="flex h-full items-center justify-center text-zinc/30">
								<div class="text-center">
									<svg class="mx-auto h-16 w-16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><path d="M20 21v-2a4 4 0 00-4-4H8a4 4 0 00-4 4v2" /><circle cx="12" cy="7" r="4" /></svg>
									<p class="mt-2 text-xs">Team Member Photo</p>
								</div>
							</div>
						</div>
						<h3 class="mt-4 font-display text-lg tracking-wide text-white">{member.name.toUpperCase()}</h3>
						<p class="text-sm text-amber/80">{member.role}</p>
					</div>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- CTA -->
<section class="relative overflow-hidden bg-black py-28">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="relative mx-auto max-w-4xl px-6 text-center lg:px-8">
		<RevealOnScroll>
			<h2 class="font-display text-5xl tracking-wide text-white lg:text-6xl">
				READY TO TRANSFORM YOUR OUTDOOR SPACE?
			</h2>
			<p class="mx-auto mt-6 max-w-xl text-lg text-zinc">
				Let's discuss your project and create something extraordinary together.
			</p>
			<a
				href="/contact"
				class="mt-10 inline-flex items-center gap-2 bg-amber px-8 py-4 text-sm font-bold uppercase tracking-wider text-black transition-all hover:bg-gold"
			>
				Get Your Free Quote
			</a>
		</RevealOnScroll>
	</div>
</section>
