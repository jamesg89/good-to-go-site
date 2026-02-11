<script lang="ts">
	import type { Snippet } from 'svelte';

	let { children, class: className = '', delay = 0 }: { children: Snippet; class?: string; delay?: number } = $props();

	let el: HTMLDivElement;
	let visible = $state(false);

	$effect(() => {
		const observer = new IntersectionObserver(
			([entry]) => {
				if (entry.isIntersecting) {
					visible = true;
					observer.unobserve(el);
				}
			},
			{ threshold: 0.1, rootMargin: '0px 0px -50px 0px' }
		);
		observer.observe(el);
		return () => observer.disconnect();
	});
</script>

<div
	bind:this={el}
	class="reveal {className}"
	class:visible
	style={delay ? `transition-delay: ${delay}ms` : ''}
>
	{@render children()}
</div>
