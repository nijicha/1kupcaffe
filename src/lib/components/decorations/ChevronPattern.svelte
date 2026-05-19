<script lang="ts">
	interface Props {
		count?: number;
		color?: string;
		opacity?: number;
		direction?: 'up' | 'down' | 'left' | 'right';
	}

	let { count = 5, color = 'currentColor', opacity = 0.4, direction = 'down' } = $props();

	const rotations = {
		up: 180,
		down: 0,
		left: 90,
		right: 270,
	};
</script>

<svg viewBox="0 0 200 200" class="w-32 h-32" style="transform: rotate({rotations[direction]}deg)">
	{#each Array.from({ length: count }, (_, i) => i) as i}
		<polyline
			points="20,{40 + i * 20} 100,{80 + i * 20} 180,{40 + i * 20}"
			fill="none"
			stroke={color}
			stroke-width="2"
			stroke-linecap="round"
			stroke-linejoin="round"
			opacity={opacity - i * (opacity / count)}
		/>
	{/each}
</svg>

<style>
	svg {
		color: var(--color-brand-sage);
	}
</style>
