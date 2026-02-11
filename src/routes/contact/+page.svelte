<script lang="ts">
	import RevealOnScroll from '$lib/components/RevealOnScroll.svelte';
	import ContactForm from '$lib/components/ContactForm.svelte';
</script>

<svelte:head>
	<title>Contact | Good To Go Contracting</title>
</svelte:head>

<!-- Hero -->
<section class="relative flex min-h-[50vh] items-center overflow-hidden bg-black">
	<div class="grain absolute inset-0"></div>
	<div class="grid-pattern absolute inset-0"></div>
	<div class="absolute top-0 right-0 h-full w-1/3 bg-amber/[0.03]" style="clip-path: polygon(40% 0, 100% 0, 100% 100%, 0% 100%)"></div>

	<div class="relative mx-auto max-w-7xl px-6 py-32 lg:px-8">
		<div class="max-w-2xl">
			<span class="font-display text-sm tracking-[0.2em] text-amber">GET IN TOUCH</span>
			<h1 class="animate-fade-up mt-4 font-display text-5xl tracking-wide text-white lg:text-7xl">
				LET'S BUILD SOMETHING GREAT
			</h1>
			<p class="animate-fade-up mt-6 text-lg text-zinc" style="animation-delay: 100ms">
				Ready to transform your outdoor space? We'd love to hear about your project.
				Reach out for a free consultation and estimate.
			</p>
		</div>
	</div>
</section>

<!-- Contact Content -->
<section class="bg-obsidian py-20 lg:py-28">
	<div class="mx-auto max-w-7xl px-6 lg:px-8">
		<div class="grid gap-16 lg:grid-cols-5">
			<!-- Contact Info -->
			<div class="lg:col-span-2">
				<RevealOnScroll>
					<div>
						<span class="font-display text-sm tracking-[0.2em] text-amber">CONTACT INFO</span>
						<h2 class="mt-2 font-display text-3xl tracking-wide text-white">
							WE'RE HERE TO HELP
						</h2>
						<div class="mt-4 h-px w-16 bg-amber"></div>
						<p class="mt-4 text-zinc leading-relaxed">
							Have a question about our services or want to discuss your project?
							Fill out the form or reach us directly using the contact info below.
						</p>
					</div>

					<div class="mt-10 space-y-8">
						<div class="flex items-start gap-4">
							<div class="flex h-10 w-10 shrink-0 items-center justify-center border border-white/10 bg-graphite">
								<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07 19.5 19.5 0 01-6-6A19.79 19.79 0 012.12 4.11 2 2 0 014.11 2h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L8.09 9.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 16.92z" />
								</svg>
							</div>
							<div>
								<h3 class="text-sm font-semibold text-white">Phone</h3>
								<p class="mt-1 text-zinc">(555) 123-4567</p>
								<p class="text-xs text-zinc/60">Mon-Fri 8am-6pm, Sat 9am-2pm</p>
							</div>
						</div>

						<div class="flex items-start gap-4">
							<div class="flex h-10 w-10 shrink-0 items-center justify-center border border-white/10 bg-graphite">
								<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z" />
									<path d="M22 6l-10 7L2 6" />
								</svg>
							</div>
							<div>
								<h3 class="text-sm font-semibold text-white">Email</h3>
								<p class="mt-1 text-zinc">info@goodtogocontracting.com</p>
								<p class="text-xs text-zinc/60">We respond within 24 hours</p>
							</div>
						</div>

						<div class="flex items-start gap-4">
							<div class="flex h-10 w-10 shrink-0 items-center justify-center border border-white/10 bg-graphite">
								<svg class="h-4 w-4 text-amber" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.5">
									<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z" />
									<circle cx="12" cy="10" r="3" />
								</svg>
							</div>
							<div>
								<h3 class="text-sm font-semibold text-white">Service Area</h3>
								<p class="mt-1 text-zinc">Serving the Greater Metro Area</p>
								<p class="text-xs text-zinc/60">Free on-site consultations</p>
							</div>
						</div>
					</div>

					<!-- Social Links -->
					<div class="mt-10 border-t border-white/5 pt-8">
						<h3 class="font-display text-xs tracking-[0.15em] text-amber">FOLLOW US</h3>
						<div class="mt-4 flex gap-2">
							<a href="/" class="flex h-10 w-10 items-center justify-center border border-white/10 bg-white/5 text-zinc transition-all hover:border-amber/50 hover:bg-amber/10 hover:text-amber" aria-label="Facebook">
								<svg class="h-4 w-4" fill="currentColor" viewBox="0 0 24 24"><path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z" /></svg>
							</a>
							<a href="/" class="flex h-10 w-10 items-center justify-center border border-white/10 bg-white/5 text-zinc transition-all hover:border-amber/50 hover:bg-amber/10 hover:text-amber" aria-label="Instagram">
								<svg class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2"><rect x="2" y="2" width="20" height="20" rx="5" /><circle cx="12" cy="12" r="5" /><circle cx="17.5" cy="6.5" r="1.5" fill="currentColor" stroke="none" /></svg>
							</a>
							<a href="/" class="flex h-10 w-10 items-center justify-center border border-white/10 bg-white/5 text-zinc transition-all hover:border-amber/50 hover:bg-amber/10 hover:text-amber" aria-label="Google">
								<svg class="h-4 w-4" fill="currentColor" viewBox="0 0 24 24"><path d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92a5.06 5.06 0 01-2.2 3.32v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.1z" /><path d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z" /><path d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z" /><path d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z" /></svg>
							</a>
						</div>
					</div>
				</RevealOnScroll>
			</div>

			<!-- Contact Form -->
			<div class="lg:col-span-3">
				<RevealOnScroll delay={100}>
					<div class="border border-white/10 bg-carbon p-8 lg:p-10">
						<h3 class="font-display text-2xl tracking-wide text-white">TELL US ABOUT YOUR PROJECT</h3>
						<p class="mt-2 text-sm text-zinc">Fill out the form below and we'll get back to you within one business day.</p>
						<div class="mt-6 h-px w-12 bg-amber"></div>
						<div class="mt-8">
							<ContactForm />
						</div>
					</div>
				</RevealOnScroll>
			</div>
		</div>
	</div>
</section>
