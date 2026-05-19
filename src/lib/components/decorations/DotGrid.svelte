<script lang="ts">
	interface Props {
		cols?: number;
		rows?: number;
		gap?: number;
		color?: string;
		opacity?: number;
	}

	let { cols = 6, rows = 6, gap = 12, color = 'currentColor', opacity = 0.3 } = $props();

	let dots = $derived.by(() =>
		Array.from({ length: rows }, (_, r) =>
			Array.from({ length: cols }, (_, c) => ({ r, c })),
		).flat()
	);

	let width = $derived((cols - 1) * gap + 24);
	let height = $derived((rows - 1) * gap + 24);
</script>

<svg viewBox="0 0 {width} {height}" class="w-full h-full" {color}>
	{#each dots as dot}
		<circle cx={dot.c * gap + 12} cy={dot.r * gap + 12} r="1.5" fill={color} {opacity} />
	{/each}
</svg>

<style>
	svg {
		color: var(--color-brand-dark);
	}
</style>
