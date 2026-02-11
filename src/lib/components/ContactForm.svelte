<script lang="ts">
	let { variant = 'dark' }: { variant?: 'light' | 'dark' } = $props();

	let formData = $state({
		name: '',
		email: '',
		phone: '',
		service: '',
		message: ''
	});

	let submitted = $state(false);

	function handleSubmit(e: Event) {
		e.preventDefault();
		submitted = true;
		setTimeout(() => (submitted = false), 4000);
	}

	const services = [
		'Landscape Design',
		'Landscape Installation',
		'Outdoor Lighting',
		'Carpentry & Concrete',
		'Earthworks & Drainage',
		'Snow & Ice Management',
		'Other'
	];

	const inputClass = 'w-full border border-white/10 bg-white/5 px-4 py-3 text-sm text-white placeholder:text-zinc transition-colors focus:border-amber/50 focus:bg-white/[0.07]';
	const labelClass = 'mb-1.5 block text-[11px] font-semibold uppercase tracking-[0.15em] text-zinc';
</script>

<form onsubmit={handleSubmit} class="space-y-5">
	<div class="grid gap-5 sm:grid-cols-2">
		<div>
			<label for="name" class={labelClass}>Full Name</label>
			<input
				type="text"
				id="name"
				bind:value={formData.name}
				required
				class={inputClass}
				placeholder="John Smith"
			/>
		</div>
		<div>
			<label for="email" class={labelClass}>Email</label>
			<input
				type="email"
				id="email"
				bind:value={formData.email}
				required
				class={inputClass}
				placeholder="john@example.com"
			/>
		</div>
	</div>

	<div class="grid gap-5 sm:grid-cols-2">
		<div>
			<label for="phone" class={labelClass}>Phone</label>
			<input
				type="tel"
				id="phone"
				bind:value={formData.phone}
				class={inputClass}
				placeholder="(555) 123-4567"
			/>
		</div>
		<div>
			<label for="service" class={labelClass}>Service Needed</label>
			<select
				id="service"
				bind:value={formData.service}
				class={inputClass}
			>
				<option value="">Select a service...</option>
				{#each services as service}
					<option value={service}>{service}</option>
				{/each}
			</select>
		</div>
	</div>

	<div>
		<label for="message" class={labelClass}>Project Details</label>
		<textarea
			id="message"
			bind:value={formData.message}
			rows={5}
			required
			class="{inputClass} resize-none"
			placeholder="Tell us about your project, timeline, and any specific requirements..."
		></textarea>
	</div>

	<button
		type="submit"
		class="relative w-full overflow-hidden border border-amber bg-amber px-8 py-4 text-sm font-bold uppercase tracking-wider text-black transition-all hover:bg-gold sm:w-auto"
	>
		{#if submitted}
			<span class="animate-fade-in">Message Sent!</span>
		{:else}
			Send Message
		{/if}
	</button>
</form>
