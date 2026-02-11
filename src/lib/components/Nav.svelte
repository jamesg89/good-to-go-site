<script lang="ts">
	import { page } from '$app/state';
	import logo from '$lib/assets/goodtogo-logo.png';

	let scrolled = $state(false);
	let mobileOpen = $state(false);
	let servicesOpen = $state(false);

	const services = [
		{ name: 'Landscape Design', href: '/services/landscape-design', icon: 'pencil' },
		{ name: 'Landscape Installation', href: '/services/landscape-installation', icon: 'shovel' },
		{ name: 'Outdoor Lighting', href: '/services/outdoor-lighting', icon: 'light' },
		{ name: 'Carpentry & Concrete', href: '/services/carpentry-concrete', icon: 'hammer' },
		{ name: 'Earthworks & Drainage', href: '/services/earthworks-drainage', icon: 'earth' },
		{ name: 'Snow & Ice Management', href: '/services/snow-ice-management', icon: 'snow' }
	];

	const navLinks = [
		{ name: 'About', href: '/about' },
		{ name: 'Portfolio', href: '/portfolio' },
		{ name: 'Blog', href: '/blog' },
		{ name: 'Contact', href: '/contact' }
	];

	$effect(() => {
		const handleScroll = () => {
			scrolled = window.scrollY > 20;
		};
		window.addEventListener('scroll', handleScroll, { passive: true });
		handleScroll();
		return () => window.removeEventListener('scroll', handleScroll);
	});

	function closeAll() {
		mobileOpen = false;
		servicesOpen = false;
	}
</script>

<nav
	class="fixed top-0 right-0 left-0 z-50 transition-all duration-500 {scrolled
		? 'bg-black/95 backdrop-blur-md border-b border-white/5'
		: ''}"
>
	<div class="mx-auto flex max-w-7xl items-center justify-between px-6 py-5 lg:px-8">
		<!-- Logo -->
		<a href="/" class="group flex items-center gap-3" onclick={closeAll}>
			<img src={logo} alt="Good To Go Contracting" class="h-16 w-auto brightness-110" />
		</a>

		<!-- Desktop Nav -->
		<div class="hidden items-center gap-0 lg:flex">
			<!-- Services Dropdown -->
			<!-- svelte-ignore a11y_no_static_element_interactions -->
			<div class="relative" onmouseleave={() => (servicesOpen = false)}>
				<button
					class="flex items-center gap-1 px-4 py-2 text-sm font-medium text-white/60 transition-colors hover:text-white"
					onmouseenter={() => (servicesOpen = true)}
				>
					Services
					<svg
						class="h-3 w-3 transition-transform duration-300 {servicesOpen ? 'rotate-180' : ''}"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						stroke-width="2"
					>
						<path d="M19 9l-7 7-7-7" />
					</svg>
				</button>

				{#if servicesOpen}
					<div class="absolute top-full left-0 mt-3 w-72 animate-scale-in border border-white/10 bg-carbon p-1.5 shadow-2xl">
						{#each services as service}
							<a
								href={service.href}
								class="group flex items-center gap-3 px-4 py-3 transition-colors hover:bg-white/5"
								onclick={closeAll}
							>
								<div class="flex h-7 w-7 shrink-0 items-center justify-center border border-white/10 bg-graphite transition-colors group-hover:border-amber/30 group-hover:bg-amber/10">
									{#if service.icon === 'pencil'}
										<svg class="h-3.5 w-3.5 text-zinc group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M11 4H4a2 2 0 00-2 2v14a2 2 0 002 2h14a2 2 0 002-2v-7" /><path d="M18.5 2.5a2.121 2.121 0 013 3L12 15l-4 1 1-4 9.5-9.5z" /></svg>
									{:else if service.icon === 'shovel'}
										<svg class="h-3.5 w-3.5 text-zinc group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M14.7 6.3a1 1 0 000 1.4l1.6 1.6a1 1 0 001.4 0l3.77-3.77a6 6 0 01-7.94 7.94l-6.91 6.91a2.12 2.12 0 01-3-3l6.91-6.91a6 6 0 017.94-7.94l-3.76 3.76z" /></svg>
									{:else if service.icon === 'light'}
										<svg class="h-3.5 w-3.5 text-zinc group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M9 18h6M10 22h4M12 2v1M4.22 4.22l.71.71M1 12h1m17 0h1m-2.93-6.07l.71-.71M12 6a6 6 0 00-4 10.47V18h8v-1.53A6 6 0 0012 6z" /></svg>
									{:else if service.icon === 'hammer'}
										<svg class="h-3.5 w-3.5 text-zinc group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M2 22l4-4m0 0l8-8m-8 8l-2-2m10 2l8-8-6-6-8 8m0 0L4 6l4 4" /></svg>
									{:else if service.icon === 'earth'}
										<svg class="h-3.5 w-3.5 text-zinc group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10" /><path d="M2 12h20M12 2a15.3 15.3 0 014 10 15.3 15.3 0 01-4 10 15.3 15.3 0 01-4-10 15.3 15.3 0 014-10z" /></svg>
									{:else if service.icon === 'snow'}
										<svg class="h-3.5 w-3.5 text-zinc group-hover:text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><path d="M12 2v20m5-17l-5 3-5-3m10 14l-5-3-5 3M2 12h20M5 5l3 5-3 5m14-10l-3 5 3 5" /></svg>
									{/if}
								</div>
								<span class="text-sm text-ash transition-colors group-hover:text-white">{service.name}</span>
							</a>
						{/each}
					</div>
				{/if}
			</div>

			{#each navLinks as link}
				<a
					href={link.href}
					class="px-4 py-2 text-sm font-medium transition-colors {page.url.pathname === link.href
						? 'text-amber'
						: 'text-white/60 hover:text-white'}"
					onclick={closeAll}
				>
					{link.name}
				</a>
			{/each}

			<div class="ml-6 h-5 w-px bg-white/10"></div>

			<a
				href="/contact"
				class="ml-6 border border-amber bg-amber/10 px-6 py-2.5 text-sm font-semibold text-amber transition-all hover:bg-amber hover:text-black"
			>
				Request a Quote
			</a>
		</div>

		<!-- Mobile Toggle -->
		<button
			class="flex h-10 w-10 items-center justify-center text-white lg:hidden"
			onclick={() => (mobileOpen = !mobileOpen)}
			aria-label="Toggle menu"
		>
			{#if mobileOpen}
				<svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
					<path d="M6 18L18 6M6 6l12 12" />
				</svg>
			{:else}
				<svg class="h-5 w-5" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
					<path d="M4 6h16M4 12h10M4 18h16" />
				</svg>
			{/if}
		</button>
	</div>

	<!-- Mobile Menu -->
	{#if mobileOpen}
		<div class="animate-fade-in border-t border-white/5 bg-carbon lg:hidden">
			<div class="mx-auto max-w-7xl px-6 py-6">
				<!-- Services Accordion -->
				<div class="border-b border-white/5 pb-4">
					<button
						class="flex w-full items-center justify-between py-3 text-sm font-semibold text-white"
						onclick={() => (servicesOpen = !servicesOpen)}
					>
						Services
						<svg
							class="h-4 w-4 text-zinc transition-transform {servicesOpen ? 'rotate-180' : ''}"
							fill="none"
							viewBox="0 0 24 24"
							stroke="currentColor"
							stroke-width="2"
						>
							<path d="M19 9l-7 7-7-7" />
						</svg>
					</button>
					{#if servicesOpen}
						<div class="mt-1 space-y-1 border-l border-amber/20 pl-4">
							{#each services as service}
								<a
									href={service.href}
									class="block py-2 text-sm text-zinc transition-colors hover:text-amber"
									onclick={closeAll}
								>
									{service.name}
								</a>
							{/each}
						</div>
					{/if}
				</div>

				{#each navLinks as link}
					<a
						href={link.href}
						class="block border-b border-white/5 py-4 text-sm font-semibold text-white transition-colors hover:text-amber"
						onclick={closeAll}
					>
						{link.name}
					</a>
				{/each}

				<a
					href="/contact"
					class="mt-6 block border border-amber bg-amber/10 py-3 text-center text-sm font-semibold text-amber transition-all hover:bg-amber hover:text-black"
					onclick={closeAll}
				>
					Request a Quote
				</a>
			</div>
		</div>
	{/if}
</nav>
