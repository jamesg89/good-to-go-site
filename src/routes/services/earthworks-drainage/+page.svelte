<script lang="ts">
	import ServicePage from '$lib/components/ServicePage.svelte';
</script>

<svelte:head>
	<title>Earthworks & Drainage | Good To Go Contracting</title>
</svelte:head>

<ServicePage
	title="Earthworks & Drainage"
	subtitle="Site Work Services"
	description="Professional grading, excavation, and drainage solutions that protect your property's foundation and create the stable base every great landscape needs."
	features={[
		{
			title: 'Property Grading & Leveling',
			description:
				'Precision grading to direct water away from foundations, create usable lawn areas, and establish proper slopes for patios, driveways, and planting beds.'
		},
		{
			title: 'French Drains & Catch Basins',
			description:
				'Subsurface drainage systems that capture and redirect groundwater before it reaches your foundation, basement, or low-lying areas of your yard.'
		},
		{
			title: 'Erosion Control',
			description:
				'Retaining walls, terracing, ground cover plantings, and erosion blankets that stabilize slopes and prevent soil loss during heavy rains.'
		},
		{
			title: 'Excavation & Hauling',
			description:
				'From small backyard digs to large-scale excavation projects, we have the equipment and expertise to move earth safely and efficiently.'
		}
	]}
	process={[
		{
			step: '01',
			title: 'Site Assessment',
			description:
				'We evaluate your property\'s topography, soil composition, water flow patterns, and existing drainage to identify the root cause of any issues.'
		},
		{
			step: '02',
			title: 'Engineering & Design',
			description:
				'Based on our assessment, we design a drainage solution that addresses current problems and prevents future issues, with a clear scope and estimate.'
		},
		{
			step: '03',
			title: 'Earthwork & Installation',
			description:
				'Our crews execute the grading, trenching, pipe installation, and backfill work with precision, ensuring proper slopes and connections throughout.'
		},
		{
			step: '04',
			title: 'Testing & Restoration',
			description:
				'We test the entire system, verify proper water flow, restore disturbed areas with topsoil and seed, and ensure your yard looks better than before.'
		}
	]}
/>
