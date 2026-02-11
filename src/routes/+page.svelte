<script lang="ts">
	import RevealOnScroll from '$lib/components/RevealOnScroll.svelte';
	import ContactForm from '$lib/components/ContactForm.svelte';
	import heroImage from '$lib/assets/Hero-Landsacping-Backyard-lawn-GoodToGo-1280.jpg';

	const services = [
		{
			name: 'Landscape Design',
			href: '/services/landscape-design',
			description: 'Custom designs that bring your outdoor vision to life with detailed plans and 3D renders.',
			icon: 'design',
			num: '01'
		},
		{
			name: 'Landscape Installation',
			href: '/services/landscape-installation',
			description: 'Expert installation of gardens, patios, retaining walls, and complete outdoor living spaces.',
			icon: 'install',
			num: '02'
		},
		{
			name: 'Outdoor Lighting',
			href: '/services/outdoor-lighting',
			description: 'Architectural and landscape lighting that transforms your property after dark.',
			icon: 'light',
			num: '03'
		},
		{
			name: 'Carpentry & Concrete',
			href: '/services/carpentry-concrete',
			description: 'Custom decks, pergolas, stamped concrete, and decorative hardscape elements.',
			icon: 'hammer',
			num: '04'
		},
		{
			name: 'Earthworks & Drainage',
			href: '/services/earthworks-drainage',
			description: 'Grading, excavation, and drainage solutions to protect your property foundation.',
			icon: 'earth',
			num: '05'
		},
		{
			name: 'Snow & Ice Management',
			href: '/services/snow-ice-management',
			description: 'Reliable commercial and residential snow removal and de-icing services.',
			icon: 'snow',
			num: '06'
		}
	];

	const testimonials = [
		{
			name: 'Sarah M.',
			text: 'Good To Go completely transformed our backyard. The attention to detail on our patio and garden installation was incredible. We now have the outdoor living space we always dreamed of.',
			project: 'Full Backyard Renovation'
		},
		{
			name: 'James & Kelly R.',
			text: 'From the initial design consultation to the final walkthrough, the professionalism was outstanding. Our new outdoor lighting makes our home look like a magazine cover.',
			project: 'Landscape Lighting Design'
		},
		{
			name: 'David T.',
			text: 'We hired them for a drainage issue that other contractors couldn\'t solve. Not only did they fix the problem, but they turned the area into a beautiful rain garden.',
			project: 'Drainage & Garden Installation'
		}
	];

	const stats = [
		{ value: '500+', label: 'Projects Completed' },
		{ value: '15+', label: 'Years Experience' },
		{ value: '100%', label: 'Licensed & Insured' },
		{ value: '4.9', label: 'Star Rating' }
	];
</script>

<svelte:head>
	<title>Good To Go Contracting | Premium Landscape & Hardscape Services</title>
</svelte:head>

<!-- Hero -->
<section class="relative min-h-screen overflow-hidden bg-black">
	<!-- Background layers -->
	<div class="absolute inset-0 bg-gradient-to-br from-carbon via-black to-black"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="grain absolute inset-0"></div>

	<div class="relative z-10 mx-auto max-w-7xl px-6 lg:px-8">
		<div class="grid min-h-screen items-center gap-8 lg:grid-cols-12 lg:gap-6">

			<!-- Left: Text Content -->
			<div class="pt-32 pb-8 lg:col-span-5 lg:py-32">
				<div class="animate-fade-up">
					<span class="inline-flex items-center gap-2 border border-amber/20 bg-amber/5 px-4 py-1.5 text-[11px] font-semibold uppercase tracking-[0.2em] text-amber">
						<span class="h-1.5 w-1.5 bg-amber"></span>
						Premium Landscape & Hardscape
					</span>
				</div>

				<h1 class="animate-fade-up mt-8 font-display text-5xl leading-[0.95] tracking-wide text-white sm:text-6xl xl:text-7xl" style="animation-delay: 100ms">
					EXCEPTIONAL<br />
					OUTDOOR<br />
					<span class="text-amber">LIVING SPACES</span>
				</h1>

				<p class="animate-fade-up mt-8 max-w-md text-base leading-relaxed text-zinc lg:text-lg" style="animation-delay: 200ms">
					We design and build landscapes that transform your property into something
					extraordinary. From concept to completion, every detail matters.
				</p>

				<div class="animate-fade-up mt-10 flex flex-wrap gap-4" style="animation-delay: 300ms">
					<a
						href="/contact"
						class="group inline-flex items-center gap-3 bg-amber px-8 py-4 text-sm font-bold uppercase tracking-wider text-black transition-all hover:bg-gold"
					>
						Start Your Project
						<svg class="h-4 w-4 transition-transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7" /></svg>
					</a>
					<a
						href="/portfolio"
						class="inline-flex items-center gap-2 border border-white/15 px-8 py-4 text-sm font-bold uppercase tracking-wider text-white transition-all hover:border-white/30 hover:bg-white/5"
					>
						View Our Work
					</a>
				</div>
			</div>

			<!-- Right: Hero Image Showcase -->
			<div class="relative pb-12 lg:col-span-7 lg:py-24">
				<div class="animate-fade-up" style="animation-delay: 200ms">
					<!-- Main image container -->
					<div class="relative">
						<!-- Corner bracket accents -->
						<div class="absolute -top-3 -left-3 z-20 h-10 w-10 border-t-2 border-l-2 border-amber/60"></div>
						<div class="absolute -right-3 -bottom-3 z-20 h-10 w-10 border-r-2 border-b-2 border-amber/60"></div>

						<!-- Primary image -->
						<div class="relative aspect-[4/3] overflow-hidden border border-white/10 bg-graphite lg:aspect-[16/10]">
							<img src={heroImage} alt="Featured landscape project - beautiful backyard lawn" class="h-full w-full object-cover" />

							<!-- Bottom gradient overlay for text legibility -->
							<div class="absolute inset-x-0 bottom-0 h-1/3 bg-gradient-to-t from-black/70 to-transparent"></div>

							<!-- Image caption overlay -->
							<div class="absolute right-0 bottom-0 left-0 flex items-end justify-between p-6">
								<div>
									<span class="text-[10px] font-semibold uppercase tracking-[0.15em] text-amber">Featured Project</span>
									<h3 class="mt-0.5 font-display text-xl tracking-wide text-white">YOUR BEST WORK HERE</h3>
								</div>
								<a href="/portfolio" class="group hidden items-center gap-1.5 text-xs font-medium text-white/60 transition-colors hover:text-amber sm:flex">
									View All
									<svg class="h-3 w-3 transition-transform group-hover:translate-x-0.5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7" /></svg>
								</a>
							</div>
						</div>

						<!-- Offset shadow frame for depth -->
						<div class="absolute -right-2 -bottom-2 -z-10 h-full w-full border border-white/[0.04] bg-carbon/50"></div>
					</div>

					<!-- Secondary image strip below -->
					<div class="mt-3 grid grid-cols-3 gap-3">
						{#each [
							{ label: 'Hardscape', caption: 'Patios & Walls' },
							{ label: 'Landscape', caption: 'Design & Install' },
							{ label: 'Lighting', caption: 'Outdoor Ambiance' }
						] as thumb, i}
							<div class="animate-fade-up group relative aspect-[3/2] overflow-hidden border border-white/5 bg-graphite" style="animation-delay: {350 + i * 80}ms">
								<!-- Replace placeholders with actual images:
									 <img src="/images/hero-thumb-{i+1}.jpg" alt="{thumb.label}" class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-105" /> -->
								<div class="flex h-full items-center justify-center text-zinc/15">
									<svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
								</div>

								<!-- Hover overlay -->
								<div class="absolute inset-0 flex items-end bg-gradient-to-t from-black/80 to-transparent p-3 opacity-0 transition-opacity group-hover:opacity-100">
									<div>
										<span class="text-[9px] font-semibold uppercase tracking-[0.15em] text-amber">{thumb.label}</span>
										<p class="text-xs text-white/80">{thumb.caption}</p>
									</div>
								</div>

								<!-- Bottom accent on hover -->
								<div class="absolute bottom-0 left-0 h-px w-0 bg-amber transition-all duration-500 group-hover:w-full"></div>
							</div>
						{/each}
					</div>
				</div>
			</div>
		</div>

		<!-- Stats bar - full width below -->
		<div class="animate-fade-up relative -mt-4 mb-8 grid grid-cols-2 gap-px overflow-hidden border border-white/10 bg-white/5 sm:grid-cols-4 lg:mb-12" style="animation-delay: 550ms">
			{#each stats as stat, i}
				<div class="bg-black/50 p-5 text-center backdrop-blur-sm {i > 0 ? 'border-l border-white/5' : ''}">
					<div class="font-display text-3xl tracking-wider text-amber">{stat.value}</div>
					<div class="mt-1 text-[10px] font-medium uppercase tracking-[0.15em] text-zinc">{stat.label}</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<!-- Services -->
<section class="relative bg-obsidian py-28 lg:py-36">
	<div class="grain absolute inset-0"></div>
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="flex flex-col items-start gap-4 lg:flex-row lg:items-end lg:justify-between">
				<div>
					<span class="font-display text-sm tracking-[0.2em] text-amber">WHAT WE DO</span>
					<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">OUR SERVICES</h2>
				</div>
				<p class="max-w-md text-sm leading-relaxed text-zinc">
					From initial concept to finished project, we deliver comprehensive outdoor solutions
					tailored to your property and lifestyle.
				</p>
			</div>
			<div class="mt-8 h-px bg-gradient-to-r from-amber/40 via-white/10 to-transparent"></div>
		</RevealOnScroll>

		<div class="stagger mt-12 grid gap-4 sm:grid-cols-2 lg:grid-cols-3">
			{#each services as service, i}
				<RevealOnScroll delay={i * 60}>
					<a
						href={service.href}
						class="group relative flex flex-col border border-white/5 bg-carbon/50 p-7 transition-all hover:border-amber/20 hover:bg-carbon"
					>
						<!-- Number -->
						<span class="font-display text-sm tracking-wider text-amber/30 transition-colors group-hover:text-amber/60">{service.num}</span>

						<!-- Icon -->
						<div class="mt-4 mb-4 flex h-10 w-10 items-center justify-center border border-white/10 bg-graphite transition-all group-hover:border-amber/30 group-hover:bg-amber/10">
							{#if service.icon === 'design'}
								<svg class="h-5 w-5 text-zinc transition-colors group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M11 4H4a2 2 0 00-2 2v14a2 2 0 002 2h14a2 2 0 002-2v-7" /><path d="M18.5 2.5a2.121 2.121 0 013 3L12 15l-4 1 1-4 9.5-9.5z" /></svg>
							{:else if service.icon === 'install'}
								<svg class="h-5 w-5 text-zinc transition-colors group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z" /></svg>
							{:else if service.icon === 'light'}
								<svg class="h-5 w-5 text-zinc transition-colors group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M9 18h6M10 22h4M12 2v1M4.22 4.22l.71.71M1 12h1m17 0h1m-2.93-6.07l.71-.71M12 6a6 6 0 00-4 10.47V18h8v-1.53A6 6 0 0012 6z" /></svg>
							{:else if service.icon === 'hammer'}
								<svg class="h-5 w-5 text-zinc transition-colors group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M2 22l4-4m0 0l8-8m-8 8l-2-2m10 2l8-8-6-6-8 8m0 0L4 6l4 4" /></svg>
							{:else if service.icon === 'earth'}
								<svg class="h-5 w-5 text-zinc transition-colors group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="10" /><path d="M2 12h20M12 2a15.3 15.3 0 014 10 15.3 15.3 0 01-4 10 15.3 15.3 0 01-4-10 15.3 15.3 0 014-10z" /></svg>
							{:else if service.icon === 'snow'}
								<svg class="h-5 w-5 text-zinc transition-colors group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5"><path d="M12 2v20m5-17l-5 3-5-3m10 14l-5-3-5 3M2 12h20M5 5l3 5-3 5m14-10l-3 5 3 5" /></svg>
							{/if}
						</div>

						<h3 class="font-display text-xl tracking-wide text-white">{service.name.toUpperCase()}</h3>
						<p class="mt-2 flex-1 text-sm leading-relaxed text-zinc">{service.description}</p>

						<div class="mt-6 flex items-center gap-2 text-sm font-medium text-zinc transition-colors group-hover:text-amber">
							Learn More
							<svg class="h-3.5 w-3.5 transition-transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7" /></svg>
						</div>

						<!-- Bottom accent line on hover -->
						<div class="absolute bottom-0 left-0 h-px w-0 bg-amber transition-all duration-500 group-hover:w-full"></div>
					</a>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- About Teaser -->
<section class="relative overflow-hidden bg-carbon py-28 lg:py-36">
	<div class="grain absolute inset-0"></div>
	<!-- Angled background element -->
	<div class="absolute top-0 left-0 h-full w-2/3 bg-graphite/30" style="clip-path: polygon(0 0, 80% 0, 60% 100%, 0 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 lg:px-8">
		<div class="grid items-center gap-16 lg:grid-cols-2">
			<RevealOnScroll>
				<div>
					<span class="font-display text-sm tracking-[0.2em] text-amber">ABOUT US</span>
					<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">
						CRAFTSMANSHIP<br />YOU CAN TRUST
					</h2>
					<div class="mt-4 h-px w-20 bg-amber"></div>
					<p class="mt-6 text-lg leading-relaxed text-ash">
						Good To Go Contracting was founded on a simple belief: your outdoor space should be as
						thoughtfully designed and expertly built as the home it surrounds. We bring years of
						experience, genuine care, and uncompromising quality to every project.
					</p>
					<p class="mt-4 text-zinc">
						From intimate garden redesigns to full-scale landscape transformations, our team handles
						every phase in-house, ensuring consistency and quality from the first sketch to the final stone.
					</p>
					<a
						href="/about"
						class="group mt-8 inline-flex items-center gap-2 border border-white/15 px-6 py-3 text-sm font-semibold text-white transition-all hover:border-amber hover:bg-amber hover:text-black"
					>
						Our Story
						<svg class="h-4 w-4 transition-transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7" /></svg>
					</a>
				</div>
			</RevealOnScroll>

			<RevealOnScroll delay={150}>
				<div class="relative">
					<div class="aspect-[4/3] overflow-hidden border border-white/10 bg-graphite">
						<div class="flex h-full items-center justify-center text-zinc/30">
							<div class="text-center">
								<svg class="mx-auto h-16 w-16" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
								<p class="mt-2 text-sm">Team / Project Photo</p>
							</div>
						</div>
					</div>
					<!-- Corner accent -->
					<div class="absolute -right-3 -bottom-3 h-16 w-16 border-r-2 border-b-2 border-amber/40"></div>
					<div class="absolute -top-3 -left-3 h-16 w-16 border-t-2 border-l-2 border-amber/40"></div>
				</div>
			</RevealOnScroll>
		</div>
	</div>
</section>

<!-- Portfolio Preview -->
<section class="bg-black py-28 lg:py-36">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="flex flex-wrap items-end justify-between gap-6">
				<div>
					<span class="font-display text-sm tracking-[0.2em] text-amber">OUR WORK</span>
					<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">FEATURED PROJECTS</h2>
				</div>
				<a
					href="/portfolio"
					class="group inline-flex items-center gap-2 text-sm font-medium text-zinc transition-colors hover:text-amber"
				>
					View Full Portfolio
					<svg class="h-4 w-4 transition-transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 12h14M12 5l7 7-7 7" /></svg>
				</a>
			</div>
			<div class="mt-6 h-px bg-gradient-to-r from-amber/40 via-white/10 to-transparent"></div>
		</RevealOnScroll>

		<div class="stagger mt-12 grid gap-3 sm:grid-cols-2 lg:grid-cols-3">
			{#each [
				{ title: 'Modern Patio & Fire Pit', category: 'Landscape Installation', aspect: 'aspect-[4/3]' },
				{ title: 'Hillside Retaining Walls', category: 'Earthworks & Drainage', aspect: 'aspect-square' },
				{ title: 'Outdoor Kitchen Build', category: 'Carpentry & Concrete', aspect: 'aspect-[3/4]' },
				{ title: 'Garden Pathway Lighting', category: 'Outdoor Lighting', aspect: 'aspect-[3/4]' },
				{ title: 'Full Property Landscape', category: 'Landscape Design', aspect: 'aspect-square' },
				{ title: 'Stamped Concrete Patio', category: 'Carpentry & Concrete', aspect: 'aspect-[4/3]' }
			] as project, i}
				<RevealOnScroll delay={i * 60}>
					<a href="/portfolio" class="img-zoom group block">
						<div class="relative {project.aspect} overflow-hidden border border-white/5 bg-graphite">
							<div class="flex h-full items-center justify-center text-zinc/20">
								<div class="text-center">
									<svg class="mx-auto h-12 w-12" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
									<p class="mt-2 text-xs">{project.title}</p>
								</div>
							</div>
							<!-- Overlay on hover -->
							<div class="absolute inset-0 flex items-end bg-gradient-to-t from-black/90 via-black/30 to-transparent p-6 opacity-0 transition-opacity group-hover:opacity-100">
								<div>
									<span class="text-[10px] font-semibold uppercase tracking-[0.15em] text-amber">{project.category}</span>
									<h3 class="mt-1 font-display text-lg tracking-wide text-white">{project.title.toUpperCase()}</h3>
								</div>
							</div>
						</div>
					</a>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- Testimonials -->
<section class="relative bg-obsidian py-28 lg:py-36">
	<div class="grain absolute inset-0"></div>
	<div class="relative mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="text-center">
				<span class="font-display text-sm tracking-[0.2em] text-amber">TESTIMONIALS</span>
				<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">
					CLIENT REVIEWS
				</h2>
			</div>
		</RevealOnScroll>

		<div class="stagger mt-16 grid gap-6 md:grid-cols-3">
			{#each testimonials as testimonial, i}
				<RevealOnScroll delay={i * 80}>
					<div class="relative border border-white/5 bg-carbon p-8">
						<!-- Quote mark -->
						<div class="absolute -top-4 left-8">
							<div class="flex h-8 w-8 items-center justify-center bg-amber text-black">
								<svg class="h-4 w-4" fill="currentColor" viewBox="0 0 24 24"><path d="M14.017 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151c-2.432.917-3.995 3.638-3.995 5.849h4v10H14.017zM0 21v-7.391c0-5.704 3.731-9.57 8.983-10.609l.995 2.151C7.546 6.068 5.983 8.789 5.983 11h4v10H0z" /></svg>
							</div>
						</div>
						<p class="mt-4 text-sm leading-relaxed text-ash italic">"{testimonial.text}"</p>
						<div class="mt-6 border-t border-white/5 pt-4">
							<div class="text-sm font-semibold text-white">{testimonial.name}</div>
							<div class="text-xs text-amber/80">{testimonial.project}</div>
						</div>
					</div>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- CTA -->
<section class="relative overflow-hidden bg-black py-28 lg:py-36">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<!-- Angled accent -->
	<div class="absolute top-0 left-0 h-full w-1/2 bg-carbon/40" style="clip-path: polygon(0 0, 80% 0, 60% 100%, 0 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 lg:px-8">
		<div class="grid items-center gap-16 lg:grid-cols-2">
			<RevealOnScroll>
				<div>
					<span class="font-display text-sm tracking-[0.2em] text-amber">READY TO START?</span>
					<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">
						TELL US ABOUT<br />YOUR PROJECT
					</h2>
					<div class="mt-4 h-px w-20 bg-amber"></div>
					<p class="mt-6 text-lg text-zinc">
						Whether you have a detailed plan or just an idea, we'd love to hear about it.
						Get a free consultation and estimate for your outdoor project.
					</p>

					<div class="mt-10 space-y-5">
						<div class="flex items-center gap-4">
							<div class="flex h-8 w-8 shrink-0 items-center justify-center border border-amber/30 bg-amber/10">
								<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 13l4 4L19 7" /></svg>
							</div>
							<span class="text-sm text-ash">Free on-site consultation & detailed estimate</span>
						</div>
						<div class="flex items-center gap-4">
							<div class="flex h-8 w-8 shrink-0 items-center justify-center border border-amber/30 bg-amber/10">
								<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 13l4 4L19 7" /></svg>
							</div>
							<span class="text-sm text-ash">Fully licensed, bonded, and insured</span>
						</div>
						<div class="flex items-center gap-4">
							<div class="flex h-8 w-8 shrink-0 items-center justify-center border border-amber/30 bg-amber/10">
								<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 13l4 4L19 7" /></svg>
							</div>
							<span class="text-sm text-ash">Quality workmanship guarantee on every project</span>
						</div>
					</div>
				</div>
			</RevealOnScroll>

			<RevealOnScroll delay={150}>
				<div class="border border-white/10 bg-carbon/60 p-8 backdrop-blur-sm">
					<ContactForm />
				</div>
			</RevealOnScroll>
		</div>
	</div>
</section>
