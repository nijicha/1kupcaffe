<script lang="ts">
	interface Props {
		color?: string;
		opacity?: number;
		count?: number;
	}

	let { color = 'currentColor', opacity = 1, count = 5 } = $props();
</script>

<svg viewBox="0 0 200 200" class="w-48 h-48" {color} {opacity}>
	{#each Array.from({ length: count }, (_, i) => i) as i}
		<path
			d="M {30 + i * 10},50 Q {100},150 {170 - i * 10},50"
			fill="none"
			stroke={color}
			stroke-width="1.5"
			opacity={opacity - i * (opacity / count)}
		/>
	{/each}
</svg>

<style>
	svg {
		color: var(--color-brand-sage);
	}
</style>
