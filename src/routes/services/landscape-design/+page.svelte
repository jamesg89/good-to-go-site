<script lang="ts">
	import ServicePage from '$lib/components/ServicePage.svelte';
</script>

<svelte:head>
	<title>Landscape Design | Good To Go Contracting</title>
</svelte:head>

<ServicePage
	title="Landscape Design"
	subtitle="Design Services"
	description="We create custom landscape designs that blend artistry with functionality, transforming your vision into a detailed, buildable plan tailored to your property and lifestyle."
	features={[
		{
			title: 'Custom Concept Development',
			description:
				'We work closely with you to understand your style, needs, and budget before developing a design concept that reflects your unique vision for the space.'
		},
		{
			title: 'Detailed Site Analysis',
			description:
				'Our designers assess soil conditions, sun exposure, drainage patterns, and existing features to create a plan that works with your property, not against it.'
		},
		{
			title: '3D Renderings & Walkthroughs',
			description:
				'See your future landscape before a single shovel hits the ground. Our 3D visualizations help you make confident decisions about materials, layout, and plantings.'
		},
		{
			title: 'Phased Master Planning',
			description:
				'Not ready to do it all at once? We can create a phased master plan that lets you build your dream landscape over time without losing design cohesion.'
		}
	]}
	process={[
		{
			step: '01',
			title: 'Your Vision',
			description:
				'We start with a conversation. Tell us about how you want to use your outdoor space, your aesthetic preferences, and your budget range. We listen carefully before we design.'
		},
		{
			step: '02',
			title: 'Getting On Site',
			description:
				'Our design team visits your property to take measurements, assess conditions, photograph key views, and understand the opportunities and challenges of your specific site.'
		},
		{
			step: '03',
			title: 'Initial Concept & Draft Budget',
			description:
				'We present a preliminary design concept with layout options, material suggestions, and a draft budget estimate. This is where your feedback shapes the final direction.'
		},
		{
			step: '04',
			title: 'Final Concept & Detailed Estimate',
			description:
				'After revisions, we deliver the final design package including detailed plans, 3D renders, a complete materials list, and a precise project estimate ready for installation.'
		}
	]}
/>
