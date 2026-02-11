<script lang="ts">
	import logo from '$lib/assets/goodtogo-logo.png';

	const services = [
		{ name: 'Landscape Design', href: '/services/landscape-design' },
		{ name: 'Landscape Installation', href: '/services/landscape-installation' },
		{ name: 'Outdoor Lighting', href: '/services/outdoor-lighting' },
		{ name: 'Carpentry & Concrete', href: '/services/carpentry-concrete' },
		{ name: 'Earthworks & Drainage', href: '/services/earthworks-drainage' },
		{ name: 'Snow & Ice Management', href: '/services/snow-ice-management' }
	];

	const company = [
		{ name: 'About', href: '/about' },
		{ name: 'Portfolio', href: '/portfolio' },
		{ name: 'Blog', href: '/blog' },
		{ name: 'Contact', href: '/contact' }
	];
</script>

<footer class="relative border-t border-white/5 bg-void text-white">
	<div class="relative mx-auto max-w-7xl px-6 pt-20 pb-12 lg:px-8">
		<!-- Top accent line -->
		<div class="absolute top-0 left-6 right-6 h-px bg-gradient-to-r from-amber via-amber/20 to-transparent lg:left-8 lg:right-8"></div>

		<div class="grid gap-12 lg:grid-cols-4">
			<!-- Brand -->
			<div class="lg:col-span-1">
				<a href="/" class="inline-block">
					<img src={logo} alt="Good To Go Contracting" class="h-14 w-auto brightness-110" />
				</a>
				<p class="mt-6 text-sm leading-relaxed text-zinc">
					Premium landscape design, installation, and hardscape services. Building extraordinary outdoor spaces.
				</p>
				<!-- Social -->
				<div class="mt-6 flex gap-2">
					<a
						href="/"
						class="flex h-9 w-9 items-center justify-center border border-white/10 bg-white/5 transition-all hover:border-amber/50 hover:bg-amber/10 hover:text-amber"
						aria-label="Facebook"
					>
						<svg class="h-4 w-4" fill="currentColor" viewBox="0 0 24 24">
							<path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z" />
						</svg>
					</a>
					<a
						href="/"
						class="flex h-9 w-9 items-center justify-center border border-white/10 bg-white/5 transition-all hover:border-amber/50 hover:bg-amber/10 hover:text-amber"
						aria-label="Instagram"
					>
						<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<rect x="2" y="2" width="20" height="20" rx="5" />
							<circle cx="12" cy="12" r="5" />
							<circle cx="17.5" cy="6.5" r="1.5" fill="currentColor" stroke="none" />
						</svg>
					</a>
					<a
						href="/"
						class="flex h-9 w-9 items-center justify-center border border-white/10 bg-white/5 transition-all hover:border-amber/50 hover:bg-amber/10 hover:text-amber"
						aria-label="Google"
					>
						<svg class="h-4 w-4" fill="currentColor" viewBox="0 0 24 24">
							<path d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92a5.06 5.06 0 01-2.2 3.32v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.1z" />
							<path d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z" />
							<path d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z" />
							<path d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z" />
						</svg>
					</a>
				</div>
			</div>

			<!-- Services -->
			<div>
				<h4 class="mb-5 font-display text-sm tracking-[0.15em] text-amber">SERVICES</h4>
				<ul class="space-y-3">
					{#each services as service}
						<li>
							<a href={service.href} class="text-sm text-zinc transition-colors hover:text-white">
								{service.name}
							</a>
						</li>
					{/each}
				</ul>
			</div>

			<!-- Company -->
			<div>
				<h4 class="mb-5 font-display text-sm tracking-[0.15em] text-amber">COMPANY</h4>
				<ul class="space-y-3">
					{#each company as link}
						<li>
							<a href={link.href} class="text-sm text-zinc transition-colors hover:text-white">
								{link.name}
							</a>
						</li>
					{/each}
				</ul>
			</div>

			<!-- Contact -->
			<div>
				<h4 class="mb-5 font-display text-sm tracking-[0.15em] text-amber">GET IN TOUCH</h4>
				<div class="space-y-4 text-sm text-zinc">
					<div class="flex items-start gap-3">
						<svg class="mt-0.5 h-4 w-4 shrink-0 text-amber/60" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07 19.5 19.5 0 01-6-6A19.79 19.79 0 012.12 4.11 2 2 0 014.11 2h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z" />
						</svg>
						<span>(555) 123-4567</span>
					</div>
					<div class="flex items-start gap-3">
						<svg class="mt-0.5 h-4 w-4 shrink-0 text-amber/60" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />
							<path d="M22 6l-10 7L2 6" />
						</svg>
						<span>info@goodtogocontracting.com</span>
					</div>
					<div class="flex items-start gap-3">
						<svg class="mt-0.5 h-4 w-4 shrink-0 text-amber/60" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
							<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z" />
							<circle cx="12" cy="10" r="3" />
						</svg>
						<span>Serving the Greater Metro Area</span>
					</div>
				</div>
			</div>
		</div>

		<!-- Bottom -->
		<div class="mt-16 flex flex-col items-center justify-between gap-4 border-t border-white/5 pt-8 md:flex-row">
			<p class="text-xs text-zinc/60">
				&copy; {new Date().getFullYear()} Good To Go Contracting. All rights reserved.
			</p>
			<div class="flex gap-6">
				<a href="/" class="text-xs text-zinc/60 transition-colors hover:text-zinc">Privacy Policy</a>
				<a href="/" class="text-xs text-zinc/60 transition-colors hover:text-zinc">Terms of Service</a>
			</div>
		</div>
	</div>
</footer>
