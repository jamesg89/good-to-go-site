<script lang="ts">
	import './layout.css';
	import Nav from '$lib/components/Nav.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<title>Good To Go Contracting | Premium Landscape & Hardscape</title>
	<meta
		name="description"
		content="Good To Go Contracting delivers exceptional landscape design, installation, outdoor lighting, carpentry, concrete, and earthwork services."
	/>
</svelte:head>

<Nav />
<main>
	{@render children()}
</main>
<Footer />
