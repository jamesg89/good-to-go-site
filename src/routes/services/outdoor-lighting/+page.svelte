<script lang="ts">
	import ServicePage from '$lib/components/ServicePage.svelte';
</script>

<svelte:head>
	<title>Outdoor Lighting | Good To Go Contracting</title>
</svelte:head>

<ServicePage
	title="Outdoor Lighting"
	subtitle="Lighting Services"
	description="Professional landscape and architectural lighting design that enhances safety, security, and the beauty of your property after dark. LED systems with smart controls."
	features={[
		{
			title: 'Architectural Lighting',
			description:
				'Up-lighting, down-lighting, and wall-washing techniques that highlight your home\'s best features and create dramatic curb appeal after sunset.'
		},
		{
			title: 'Landscape & Garden Lighting',
			description:
				'Path lights, spot lights, and accent fixtures that make your gardens, trees, and hardscape elements shine beautifully throughout the evening hours.'
		},
		{
			title: 'Outdoor Living Area Lighting',
			description:
				'String lights, recessed deck lights, step lighting, and ambient fixtures that make patios, pergolas, and entertainment areas usable and inviting at night.'
		},
		{
			title: 'Smart Controls & LED Systems',
			description:
				'Energy-efficient LED fixtures with smart timers, dimmers, and app-controlled zones so you get the perfect ambiance with minimal energy cost.'
		}
	]}
	process={[
		{
			step: '01',
			title: 'Evening Consultation',
			description:
				'We visit your property at dusk to assess the existing conditions, identify key features to highlight, and discuss your goals for the lighting design.'
		},
		{
			step: '02',
			title: 'Lighting Design Plan',
			description:
				'We create a detailed lighting plan showing fixture locations, beam angles, wattage, and zones, along with a fixture selection and budget estimate.'
		},
		{
			step: '03',
			title: 'Professional Installation',
			description:
				'Our team installs low-voltage LED systems with proper wiring, transformers, and connections, taking care to conceal all wiring and junction points.'
		},
		{
			step: '04',
			title: 'Fine-Tuning & Programming',
			description:
				'We return at night to aim every fixture precisely, adjust brightness levels, program timers and zones, and ensure the overall effect is exactly right.'
		}
	]}
/>
