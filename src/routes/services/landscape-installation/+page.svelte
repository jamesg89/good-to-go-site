<script lang="ts">
	import ServicePage from '$lib/components/ServicePage.svelte';
</script>

<svelte:head>
	<title>Landscape Installation | Good To Go Contracting</title>
</svelte:head>

<ServicePage
	title="Landscape Installation"
	subtitle="Installation Services"
	description="From softscaping to hardscaping, we bring landscape designs to life with expert installation of gardens, patios, walkways, retaining walls, and complete outdoor living areas."
	features={[
		{
			title: 'Softscape & Planting',
			description:
				'Gardens, trees, shrubs, perennials, ground covers, and ornamental grasses installed with proper soil prep and spacing for long-term health and beauty.'
		},
		{
			title: 'Hardscape Construction',
			description:
				'Patios, walkways, retaining walls, steps, and borders built with natural stone, pavers, or segmental block to last decades with minimal maintenance.'
		},
		{
			title: 'Water Features',
			description:
				'Pondless waterfalls, bubbling rocks, fountains, and irrigation systems that add life and sound to your landscape while managing water efficiently.'
		},
		{
			title: 'Outdoor Living Spaces',
			description:
				'Complete outdoor rooms including seating areas, fire pits, outdoor kitchens, and entertainment zones designed for year-round enjoyment.'
		}
	]}
	process={[
		{
			step: '01',
			title: 'Pre-Construction Planning',
			description:
				'We review the design plans, order materials, schedule utility locates, and coordinate logistics so installation day runs smoothly from the start.'
		},
		{
			step: '02',
			title: 'Site Preparation',
			description:
				'Proper grading, excavation, and base preparation ensure everything built on top will be level, stable, and properly drained for the long haul.'
		},
		{
			step: '03',
			title: 'Construction & Installation',
			description:
				'Our skilled crews install hardscape elements first, then softscape, following a careful sequence that protects finished work and maintains quality standards.'
		},
		{
			step: '04',
			title: 'Final Walkthrough & Care Guide',
			description:
				'We walk through the completed project together, address any details, and provide a comprehensive care guide for maintaining your new landscape.'
		}
	]}
/>
