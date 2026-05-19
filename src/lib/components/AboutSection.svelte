<script lang="ts">
	import DotGrid from './decorations/DotGrid.svelte';

	const industries = [
		'Coffee & Beverages',
		'Software & AI',
		'Logistics',
		'Engineering',
		'Renewable Energy',
	];

	const stats = [
		{ label: '3 Countries', value: 'TH, MM, LA' },
		{ label: 'SCA-Grade QC', value: '82–86 Scores' },
		{ label: 'Offline-First AI', value: 'Farmer Empowerment' },
	];
</script>

<section id="about" class="py-24 px-4 bg-white">
	<div class="max-w-7xl mx-auto">
		<h2 class="text-5xl md:text-6xl font-black text-brand-olive mb-16">About Our Business</h2>

		<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
			<!-- Left: Text -->
			<div class="space-y-6 text-lg text-brand-dark leading-relaxed">
				<p>
					1KUP CAFFE is a diversified group operating across coffee and beverages, software and AI,
					logistics, engineering, and renewable energy. We design, produce, and scale from coffee sourcing
					and RTD manufacturing to data platforms, automated warehouses, and sustainable infrastructure.
				</p>
				<p>
					With operations in Thailand and Southeast Asia, certified facilities, and a partner network
					across Myanmar coffee beans sourcing and AI tools to improve yield, quality, and traceability,
					we combine industry expertise with technology to improve quality, reduce cost, and accelerate
					time-to-market.
				</p>
				<p class="font-semibold text-brand-olive">
					Our mission is to create value responsibly—advancing circular economy practices, transparent
					supply chains, and customer success.
				</p>
			</div>

			<!-- Right: Decorations & Pills -->
			<div class="relative">
				<div class="absolute -top-8 -right-8 w-80 h-80 opacity-20">
					<DotGrid cols={8} rows={8} gap={10} />
				</div>
				<div class="relative z-10 space-y-4">
					{#each industries as industry}
						<div
							class="bg-brand-sage-light text-brand-dark rounded-full px-6 py-3 font-semibold inline-block"
						>
							{industry}
						</div>
					{/each}
				</div>
			</div>
		</div>

		<!-- Stats Row -->
		<div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-16 pt-16 border-t border-brand-sage-light">
			{#each stats as stat}
				<div>
					<div class="text-sm font-semibold text-brand-sage uppercase tracking-wide">{stat.label}</div>
					<div class="text-2xl font-black text-brand-olive mt-2">{stat.value}</div>
				</div>
			{/each}
		</div>
	</div>
</section>
