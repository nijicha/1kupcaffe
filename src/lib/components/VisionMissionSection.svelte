<script lang="ts">
	import Sparkle from './decorations/Sparkle.svelte';
	import StripedCircle from './decorations/StripedCircle.svelte';

	const visions = [
		"To be Southeast Asia's most trusted, tech-enabled coffee supply chain—uplifting farmers and delivering world-class quality.",
		'To transform Thailand, Myanmar, and Laos coffee from origin to global market through AI, transparency, and fair value for growers.',
		'To lead in responsible coffee and beverage innovation—zero-defect, fully traceable, and carbon-smart.',
		'To empower 50,000 farmers with offline-first AI and fair pricing, creating premium, ethical products for the world.',
		'To be the fastest path from farm to shelf in ASEAN—data-driven, compliant, and sustainably delivered.',
		'To make every cup traceable and every farmer prosperous through technology and partnerships.',
		"To build the region's benchmark for circular, low-waste agri supply chains.",
		'To become the partner of choice for brands seeking quality, speed, and transparent sourcing in Southeast Asia.',
	];

	const missions = [
		'Our mission is to connect Thailand, Myanmar, and Laos farmers to global markets by pairing fair pricing with offline-first AI and SCA-grade quality control, delivering premium, traceable coffee for brands worldwide.',
		'We empower Southeast Asian growers and partners with practical technology, training, and transparent trade to raise quality, cut waste, and speed time-to-market.',
		'We source and produce responsible coffee and beverages, using AI-driven processes and rigorous QA to ensure zero-defect lots, full traceability, and consistent value for customers and communities.',
		'We build resilient, compliant supply chains—sanctions-screened, food-safe, and ethically priced—so every cup improves farmer livelihoods.',
	];
</script>

<section id="vision" class="py-24 px-4 bg-brand-dark text-brand-cream">
	<div class="max-w-7xl mx-auto">
		<!-- Decorations -->
		<div class="absolute top-20 left-10 w-64 h-64 opacity-5">
			<StripedCircle size={256} opacity={0.15} />
		</div>

		<div class="grid grid-cols-1 lg:grid-cols-2 gap-16">
			<!-- Vision -->
			<div>
				<h2 class="text-5xl font-bold mb-12">Vision</h2>
				<ul class="space-y-6">
					{#each visions as vision}
						<li class="flex gap-4">
							<div class="flex-shrink-0 mt-1">
								<Sparkle size="sm" color="#c8d9be" />
							</div>
							<span class="text-lg leading-relaxed">{vision}</span>
						</li>
					{/each}
				</ul>
			</div>

			<!-- Mission -->
			<div>
				<h2 class="text-5xl font-black mb-12">Mission</h2>
				<ul class="space-y-6">
					{#each missions as mission}
						<li class="flex gap-4">
							<div class="flex-shrink-0 mt-1">
								<Sparkle size="sm" color="#c8d9be" />
							</div>
							<span class="text-lg leading-relaxed">{mission}</span>
						</li>
					{/each}
				</ul>
			</div>
		</div>
	</div>
</section>
