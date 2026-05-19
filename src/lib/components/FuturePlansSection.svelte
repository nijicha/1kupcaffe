<script lang="ts">
	import ChevronPattern from './decorations/ChevronPattern.svelte';

	const milestones = [
		{
			period: 'Now - 12 Months',
			items: [
				'QC lab in Chiang Mai for standardized origin-to-FOB services.',
				"Scale traceable coffee sourcing in Myanmar's Shan and Laos' Bolaven.",
				'Deepen partnerships in Northern Thailand.',
				'Pilot premium RTD products for ASEAN retailers.',
			],
		},
		{
			period: '12-24 Months',
			items: [
				'Strengthen third-party cupping in Vietnam.',
				'Standardize origin-to-FOB services with transparent SLAs, lot-level traceability, and <=1% shipment claims.',
				'Launch multilingual AI Academy: offline-first courses and micro-credentials for farmers, SMEs, and supply-chain teams.',
			],
		},
		{
			period: '24-36 Months',
			items: [
				'Expand bonded logistics across ASEAN to EU/US partners.',
				'Embed ESG targets: income uplift, waste reduction, and carbon-smart operations.',
				'Train 10,000 learners; onboard new farmer cooperatives each season.',
				'Integrate with client ERPs for seamless data flow.',
			],
		},
	];
</script>

<section id="future-plans" class="py-24 px-4 bg-white">
	<div class="max-w-7xl mx-auto">
		<h2 class="text-5xl md:text-6xl font-black text-brand-olive mb-16">Future Plans</h2>

		<p class="text-lg text-brand-dark max-w-3xl mb-16 leading-relaxed">
			Over the next 12–36 months, we will evolve into a global connector for sustainable trade while expanding our
			AI training footprint. We'll scale traceable coffee sourcing in Myanmar's Shan and Laos' Bolaven, deepen
			partnerships in Northern Thailand, and pilot premium RTD products for ASEAN retailers. We will open a QC lab in
			Chiang Mai, strengthen third-party cupping in Vietnam, and standardize origin-to-FOB services with transparent
			SLAs, lot-level traceability, and ≤1% shipment claims. In parallel, we'll launch our multilingual AI Academy—offline-first
			courses and micro-credentials for farmers, SMEs, and supply-chain teams—built with university, NGO, and brand
			partners. Our platform will unify buyer dashboards with learning pathways, enabling verified skills, better
			quality outcomes, and faster time-to-market. We plan to train 10,000 learners, onboard new co-ops each season,
			integrate with client ERPs for seamless data flow, and expand bonded logistics across ASEAN to EU/US partners.
			Throughout, we'll embed ESG targets—income uplift, waste reduction, and carbon-smart operations—so every
			connection we make, and every skill we teach, creates measurable value for people and the planet.
		</p>

		<!-- Timeline: Desktop -->
		<div class="hidden md:block">
			<div class="relative">
				<!-- Connecting line -->
				<div class="absolute top-12 left-0 right-0 h-1 bg-gradient-to-r from-brand-olive via-brand-sage to-brand-olive"></div>

				<!-- Milestones -->
				<div class="grid grid-cols-1 md:grid-cols-3 gap-8 relative z-10">
					{#each milestones as milestone, i}
						<div>
							<!-- Node -->
							<div class="flex flex-col items-center mb-6">
								<div class="w-12 h-12 bg-brand-olive rounded-full flex items-center justify-center text-brand-cream font-bold mb-4">
									{i + 1}
								</div>
								<h3 class="text-xl font-bold text-brand-olive text-center">{milestone.period}</h3>
							</div>

							<!-- Content -->
							<ul class="space-y-3">
								{#each milestone.items as item}
									<li class="flex gap-3">
										<span class="flex-shrink-0 text-brand-sage font-bold">•</span>
										<span class="text-brand-dark text-sm leading-relaxed">{item}</span>
									</li>
								{/each}
							</ul>
						</div>
					{/each}
				</div>
			</div>
		</div>

		<!-- Timeline: Mobile -->
		<div class="md:hidden space-y-8">
			{#each milestones as milestone, i}
				<div class="border-l-4 border-brand-olive pl-6 pb-6">
					<div class="flex items-center gap-3 mb-4">
						<div class="w-10 h-10 bg-brand-olive rounded-full flex items-center justify-center text-brand-cream font-bold">
							{i + 1}
						</div>
						<h3 class="text-lg font-bold text-brand-olive">{milestone.period}</h3>
					</div>
					<ul class="space-y-3">
						{#each milestone.items as item}
							<li class="flex gap-3">
								<span class="flex-shrink-0 text-brand-sage font-bold">•</span>
								<span class="text-brand-dark text-sm leading-relaxed">{item}</span>
							</li>
						{/each}
					</ul>
				</div>
			{/each}
		</div>
	</div>
</section>
