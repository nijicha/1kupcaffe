<script lang="ts">
	import { page } from '$app/state';
	// import { setLocale } from '$lib/paraglide/runtime';

	let isOpen = $state(false);
	let activeSection = $state<string | null>(null);

	const navItems = [
		{ label: 'About', href: '#about' },
		{ label: 'Vision', href: '#vision' },
		{ label: 'Services', href: '#services' },
		{ label: 'Products', href: '#products' },
		{ label: 'Achievements', href: '#achievements' },
		{ label: 'Contact', href: '#contact' },
	];

	// function handleLocaleSwitch(locale: string) {
	// 	setLocale(locale);
	// }
</script>

<nav class="sticky top-0 z-50 bg-brand-dark/95 backdrop-blur-sm border-b border-white/10">
	<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex justify-between items-center h-16">
			<!-- Logo -->
			<a href="/#hero" class="text-2xl font-black text-brand-cream">1KUP</a>

			<!-- Desktop Nav -->
			<div class="hidden md:flex gap-8">
				{#each navItems as item}
					<a
						href={item.href}
						class="text-sm font-semibold text-brand-cream/70 hover:text-brand-cream transition-colors"
					>
						{item.label}
					</a>
				{/each}
			</div>

			<!-- Controls -->
			<div class="flex items-center gap-4">
				<!-- Locale Switcher -->
				<!-- <div class="flex gap-2">
					<button
						onclick={() => handleLocaleSwitch('en')}
						class="px-2 py-1 text-xs font-bold rounded bg-brand-sage-light text-brand-dark hover:bg-brand-sage transition"
					>
						EN
					</button>
					<button
						onclick={() => handleLocaleSwitch('th')}
						class="px-2 py-1 text-xs font-bold rounded bg-brand-sage-light text-brand-dark hover:bg-brand-sage transition"
					>
						TH
					</button>
				</div> -->

				<!-- Mobile Menu Toggle -->
				<button
					onclick={() => (isOpen = !isOpen)}
					class="md:hidden p-2 rounded text-brand-cream hover:bg-white/10 transition"
					aria-label="Toggle menu"
				>
					<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d={isOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16M4 18h16'}
						/>
					</svg>
				</button>
			</div>
		</div>

		<!-- Mobile Nav -->
		{#if isOpen}
			<div class="md:hidden pb-4 flex flex-col gap-2">
				{#each navItems as item}
					<a
						href={item.href}
						onclick={() => (isOpen = false)}
						class="px-4 py-2 text-sm font-semibold text-brand-cream/80 hover:bg-white/10 rounded transition"
					>
						{item.label}
					</a>
				{/each}
			</div>
		{/if}
	</div>
</nav>
