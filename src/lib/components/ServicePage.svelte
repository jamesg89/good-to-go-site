<script lang="ts">
	import RevealOnScroll from '$lib/components/RevealOnScroll.svelte';
	import type { Snippet } from 'svelte';

	let {
		title,
		subtitle,
		description,
		features,
		process,
		children
	}: {
		title: string;
		subtitle: string;
		description: string;
		features: { title: string; description: string }[];
		process: { step: string; title: string; description: string }[];
		children?: Snippet;
	} = $props();
</script>

<!-- Hero -->
<section class="relative flex min-h-[55vh] items-center overflow-hidden bg-black">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="absolute top-0 right-0 h-full w-1/3 bg-amber/[0.03]" style="clip-path: polygon(40% 0, 100% 0, 100% 100%, 0% 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 py-32 lg:px-8">
		<div class="max-w-2xl">
			<span class="font-display text-sm tracking-[0.2em] text-amber">{subtitle.toUpperCase()}</span>
			<h1 class="animate-fade-up mt-4 font-display text-5xl tracking-wide text-white lg:text-7xl">
				{title.toUpperCase()}
			</h1>
			<p class="animate-fade-up mt-6 text-lg text-zinc" style="animation-delay: 100ms">
				{description}
			</p>
			<a
				href="/contact"
				class="animate-fade-up mt-8 inline-flex items-center gap-2 bg-amber px-8 py-4 text-sm font-bold uppercase tracking-wider text-black transition-all hover:bg-gold"
				style="animation-delay: 200ms"
			>
				Get a Free Quote
			</a>
		</div>
	</div>
</section>

<!-- Features -->
<section class="bg-obsidian py-24 lg:py-32">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="text-center">
				<span class="font-display text-sm tracking-[0.2em] text-amber">WHAT WE OFFER</span>
				<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">SERVICE HIGHLIGHTS</h2>
			</div>
		</RevealOnScroll>

		<div class="stagger mt-16 grid gap-5 sm:grid-cols-2">
			{#each features as feature, i}
				<RevealOnScroll delay={i * 80}>
					<div class="flex gap-5 border border-white/5 bg-carbon p-7">
						<div class="flex h-9 w-9 shrink-0 items-center justify-center border border-amber/30 bg-amber/10">
							<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M5 13l4 4L19 7" /></svg>
						</div>
						<div>
							<h3 class="font-display text-lg tracking-wide text-white">{feature.title.toUpperCase()}</h3>
							<p class="mt-1.5 text-sm leading-relaxed text-zinc">{feature.description}</p>
						</div>
					</div>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- Process -->
<section class="relative bg-carbon py-24 lg:py-32">
	<div class="grain absolute inset-0"></div>
	<div class="relative mx-auto max-w-7xl px-6 lg:px-8">
		<RevealOnScroll>
			<div class="text-center">
				<span class="font-display text-sm tracking-[0.2em] text-amber">HOW IT WORKS</span>
				<h2 class="mt-2 font-display text-5xl tracking-wide text-white lg:text-6xl">OUR PROCESS</h2>
			</div>
		</RevealOnScroll>

		<div class="mt-16 space-y-0">
			{#each process as step, i}
				<RevealOnScroll delay={i * 80}>
					<div class="grid items-center gap-8 py-10 lg:grid-cols-12 {i > 0 ? 'border-t border-white/5' : ''}">
						<div class="lg:col-span-1">
							<span class="font-display text-4xl tracking-wider text-amber/20">{step.step}</span>
						</div>
						<div class="lg:col-span-4">
							<h3 class="font-display text-2xl tracking-wide text-white">{step.title.toUpperCase()}</h3>
						</div>
						<div class="lg:col-span-5">
							<p class="leading-relaxed text-zinc">{step.description}</p>
						</div>
						<div class="lg:col-span-2">
							<div class="aspect-video overflow-hidden border border-white/5 bg-graphite">
								<div class="flex h-full items-center justify-center text-zinc/20">
									<svg class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1"><rect x="3" y="3" width="18" height="18" rx="2" /><circle cx="8.5" cy="8.5" r="1.5" /><path d="M21 15l-5-5L5 21" /></svg>
								</div>
							</div>
						</div>
					</div>
				</RevealOnScroll>
			{/each}
		</div>
	</div>
</section>

<!-- Optional extra content -->
{#if children}
	{@render children()}
{/if}

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
				Contact us today for a free on-site consultation and detailed project estimate.
			</p>
			<div class="mt-10 flex flex-wrap justify-center gap-4">
				<a
					href="/contact"
					class="inline-flex items-center gap-2 bg-amber px-8 py-4 text-sm font-bold uppercase tracking-wider text-black transition-all hover:bg-gold"
				>
					Request a Quote
				</a>
				<a
					href="/portfolio"
					class="inline-flex items-center gap-2 border border-white/15 px-8 py-4 text-sm font-bold uppercase tracking-wider text-white transition-all hover:border-white/30 hover:bg-white/5"
				>
					See Our Work
				</a>
			</div>
		</RevealOnScroll>
	</div>
</section>
