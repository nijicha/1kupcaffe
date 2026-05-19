<script lang="ts">
	interface Props {
		size?: number;
		color?: string;
		opacity?: number;
	}

	let { size = 120, color = 'currentColor', opacity = 0.5 } = $props();

	const radius = size / 2;
</script>

<svg viewBox="0 0 {size} {size}" class="w-full h-full" {color}>
	<defs>
		<pattern
			id="stripes-{Math.random()}"
			patternUnits="userSpaceOnUse"
			width="4"
			height="4"
			patternTransform="rotate(45)"
		>
			<line x1="0" y1="0" x2="0" y2="4" stroke={color} stroke-width="2" {opacity} />
		</pattern>
	</defs>
	<circle
		cx={radius}
		cy={radius}
		r={radius - 2}
		fill="url(#stripes-{Math.random()})"
		stroke="none"
	/>
	<circle cx={radius} cy={radius} r={radius - 2} fill="none" stroke={color} stroke-width="1" {opacity} />
</svg>

<style>
	svg {
		color: var(--color-brand-sage);
	}
</style>
