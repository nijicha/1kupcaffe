<script lang="ts">
	interface Props {
		size?: 'sm' | 'md' | 'lg';
		color?: string;
	}

	let { size = 'md', color = 'currentColor' } = $props();

	const sizes = {
		sm: 'w-4 h-4',
		md: 'w-6 h-6',
		lg: 'w-10 h-10',
	};
</script>

<svg viewBox="0 0 24 24" class={sizes[size]} {color}>
	<!-- Four-point star via two diamond crosses -->
	<!-- Horizontal bar -->
	<rect x="2" y="10.5" width="20" height="3" fill={color} rx="1" />
	<!-- Vertical bar -->
	<rect x="10.5" y="2" width="3" height="20" fill={color} ry="1" />
</svg>

<style>
	svg {
		color: var(--color-brand-olive);
	}
</style>
