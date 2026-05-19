<script lang="ts">
	import type { Pathname } from '$app/types';
	import { resolve } from '$app/paths';
	import { page } from '$app/state';
	import { locales, localizeHref } from '$lib/paraglide/runtime';
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<title>1KUP CAFFE — From Farm to Cup</title>
	<meta name="description" content="1KUP CAFFE is a coffee-and-technology company connecting Southeast Asian farmers to global markets through AI, traceable sourcing, and sustainable supply chains." />
	<link rel="icon" href={favicon} />
</svelte:head>
{@render children()}

<div style="display:none">
	{#each locales as locale (locale)}
		<a href={resolve(localizeHref(page.url.pathname, { locale }) as Pathname)}>{locale}</a>
	{/each}
</div>
