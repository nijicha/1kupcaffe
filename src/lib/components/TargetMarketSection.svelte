<script lang="ts">
	import ArchLines from './decorations/ArchLines.svelte';
	import Sparkle from './decorations/Sparkle.svelte';
</script>

<section id="target-market" class="py-24 px-4 bg-brand-dark text-brand-cream">
	<div class="max-w-7xl mx-auto">
		<div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
			<!-- Left: Problem & Solution -->
			<div>
				<h2 class="text-5xl font-black mb-12">Target Market</h2>

				<div class="space-y-8">
					<div>
						<h3 class="text-2xl font-bold mb-4">The Problem</h3>
						<p class="text-lg leading-relaxed">
							Coffee farmers and processors face persistent challenges: unpredictable yields, variable bean
							quality, post-harvest losses, and inefficient logistics that reduce income and limit access to
							premium markets. Smallholder cooperatives in particular lack affordable, practical tools to
							monitor crop health, grade green beans consistently, and manage the cold chain and routing
							needed to preserve quality from farm to export.
						</p>
					</div>

					<div>
						<h3 class="text-2xl font-bold mb-4">Our Solution</h3>
						<p class="text-lg leading-relaxed">
							We combine local agronomic expertise with practical AI solutions to increase yield, improve
							export-grade quality, and reduce losses. On the farm: precision agronomy, low-cost sensors, mobile
							data capture, and image-based pest, disease, and maturity detection guide irrigation,
							fertilization, and harvest timing. At processing centers: computer-vision sorting and predictive
							quality models reduce defects and standardize grading. In logistics: demand forecasting, route
							optimization, and temperature monitoring help preserve bean quality in transit and lower delivery
							costs. All data feeds a traceable farm-to-cup dashboard that supports certifications, buyer
							confidence, and better pricing for growers.
						</p>
					</div>

					<div class="bg-brand-sage/20 rounded-lg p-6 border border-brand-sage/40">
						<p class="text-xl font-bold text-brand-sage-light mb-2">Pilot Impact</p>
						<p class="text-2xl font-black text-brand-cream">10–20% increase in export-grade beans</p>
						<p class="text-sm text-brand-sage-light mt-2">within 6–9 months of deployment</p>
					</div>
				</div>
			</div>

			<!-- Right: Decorative -->
			<div class="relative hidden lg:flex items-center justify-center">
				<div class="absolute inset-0 opacity-10">
					<ArchLines count={6} opacity={0.4} />
				</div>
				<div class="relative z-10">
					<svg viewBox="0 0 200 200" class="w-64 h-64">
						<circle cx="100" cy="100" r="80" fill="none" stroke="#c8d9be" stroke-width="2" opacity="0.3" />
						<circle cx="100" cy="100" r="60" fill="none" stroke="#c8d9be" stroke-width="2" opacity="0.5" />
						<circle cx="100" cy="100" r="40" fill="none" stroke="#c8d9be" stroke-width="3" />
						<text x="100" y="110" text-anchor="middle" font-size="24" font-weight="bold" fill="#c8d9be">
							+20%
						</text>
					</svg>
				</div>
			</div>
		</div>
	</div>
</section>
