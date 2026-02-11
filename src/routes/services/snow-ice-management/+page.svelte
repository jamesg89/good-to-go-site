<script lang="ts">
	import ServicePage from '$lib/components/ServicePage.svelte';
</script>

<svelte:head>
	<title>Snow & Ice Management | Good To Go Contracting</title>
</svelte:head>

<ServicePage
	title="Snow & Ice Management"
	subtitle="Winter Services"
	description="Reliable commercial and residential snow removal and de-icing services that keep your property safe and accessible throughout the winter season."
	features={[
		{
			title: 'Snow Plowing & Removal',
			description:
				'Prompt, thorough snow clearing for driveways, parking lots, walkways, and access roads using professional-grade equipment sized for your property.'
		},
		{
			title: 'De-Icing & Salt Application',
			description:
				'Proactive and reactive ice treatment using environmentally-conscious de-icing products that prevent ice buildup while minimizing impact on your landscape.'
		},
		{
			title: 'Seasonal Contracts',
			description:
				'Lock in priority service with a seasonal contract. Guaranteed response times, consistent pricing, and peace of mind all winter long.'
		},
		{
			title: '24/7 Emergency Response',
			description:
				'When unexpected storms hit, our crews are ready around the clock. Emergency callout service ensures you\'re never snowed in for long.'
		}
	]}
	process={[
		{
			step: '01',
			title: 'Pre-Season Planning',
			description:
				'Before the first snowfall, we visit your property to map plow routes, identify sensitive areas, mark obstacles, and establish a service plan tailored to your needs.'
		},
		{
			step: '02',
			title: 'Weather Monitoring',
			description:
				'We actively monitor weather forecasts and pre-treat surfaces before storms when conditions warrant, reducing ice buildup and speeding post-storm clearing.'
		},
		{
			step: '03',
			title: 'Storm Response',
			description:
				'When trigger depths are reached, our crews deploy automatically. Plowing, shoveling, and salting happen in coordinated waves to keep your property clear.'
		},
		{
			step: '04',
			title: 'Post-Storm Cleanup',
			description:
				'After the storm passes, we return for detail work: clearing windrows, widening pathways, touching up salt application, and ensuring full accessibility.'
		}
	]}
/>
