<script lang="ts">
	import ServicePage from '$lib/components/ServicePage.svelte';
</script>

<svelte:head>
	<title>Carpentry & Concrete | Good To Go Contracting</title>
</svelte:head>

<ServicePage
	title="Carpentry & Concrete"
	subtitle="Building Services"
	description="Custom carpentry and concrete work that adds structure, function, and beauty to your outdoor space. From decks and pergolas to stamped patios and decorative walls."
	features={[
		{
			title: 'Custom Decks & Pergolas',
			description:
				'Cedar, composite, and hardwood deck construction with optional pergolas, privacy screens, and built-in seating tailored to your space and style.'
		},
		{
			title: 'Stamped & Decorative Concrete',
			description:
				'Stamped patterns, exposed aggregate, acid staining, and decorative finishes that give concrete surfaces the look of natural stone at a fraction of the cost.'
		},
		{
			title: 'Fences & Privacy Structures',
			description:
				'Custom wood and composite fencing, privacy walls, trellises, and gates that define your property with style and provide the seclusion you want.'
		},
		{
			title: 'Outdoor Structures',
			description:
				'Gazebos, arbors, storage sheds, and custom-built outdoor furniture that extend your living space and add functional beauty to your yard.'
		}
	]}
	process={[
		{
			step: '01',
			title: 'Design & Material Selection',
			description:
				'We help you choose the right materials, finishes, and design details for your project, considering aesthetics, durability, maintenance, and budget.'
		},
		{
			step: '02',
			title: 'Permits & Preparation',
			description:
				'We handle building permits, utility locates, and site preparation so everything is ready for construction to begin on schedule.'
		},
		{
			step: '03',
			title: 'Expert Construction',
			description:
				'Our experienced carpenters and concrete crews build with precision, following best practices and local codes to ensure structural integrity and lasting quality.'
		},
		{
			step: '04',
			title: 'Finishing & Inspection',
			description:
				'Final sanding, staining, sealing, and detail work brings everything together. We complete a thorough quality inspection before your final walkthrough.'
		}
	]}
/>
