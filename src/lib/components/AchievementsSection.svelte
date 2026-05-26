<script lang="ts">
	import DotGrid from './decorations/DotGrid.svelte';

	const achievements = [
		{
			title: 'Traceable Specialty Arabica',
			desc: 'SCA 82–86 consistency from Thailand, Myanmar (Shan), and Laos with ≤1% shipment claims.',
		},
		{
			title: 'Offline-First AI',
			desc: 'Available in Burmese, Shan, Thai, and Lao; guides farmers on ripeness selection, drying, and defect detection.',
		},
		{
			title: 'Cross-Border Network',
			desc: 'Myanmar–Thailand–Laos–Vietnam–Malaysia–Singapore routing with bonded options and 3PL partners.',
		},
		{
			title: 'Farmer Cooperatives',
			desc: 'Onboarded cooperatives in Myanmar, Thailand, and Laos; deployed hands-on training and quality-premium income ladders.',
		},
	];
</script>

<section id="achievements" class="py-16 px-4 bg-brand-sage-light">
	<div class="max-w-7xl mx-auto">
		<div class="absolute top-0 right-0 w-96 h-96 opacity-10">
			<DotGrid cols={10} rows={10} gap={12} />
		</div>

		<h2 class="text-5xl md:text-6xl font-bold text-brand-olive mb-8">Business Achievements</h2>

		<!-- Contact Links -->
		<div class="flex flex-wrap gap-3 mb-12">
			<a
				href="https://www.1kupcaffe.com"
				target="_blank"
				rel="noopener noreferrer"
				class="inline-block px-6 py-3 bg-brand-olive text-brand-cream font-bold rounded hover:bg-brand-dark transition"
			>
				www.1kupcaffe.com
			</a>
			<a
				href="https://instagram.com/coldbrewbyarome"
				target="_blank"
				rel="noopener noreferrer"
				class="inline-block px-6 py-3 bg-brand-sage text-brand-cream font-bold rounded hover:bg-brand-olive transition flex items-center gap-2"
			>
				<svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
					<path
						d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.466.182-.8.398-1.15.748-.35.35-.566.684-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.684.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.684.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z"
					/>
				</svg>
				@coldbrewbyarome
			</a>
		</div>

		<!-- Achievement Cards -->
		<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
			{#each achievements as achievement}
				<div class="bg-white rounded-lg p-8 border-2 border-brand-olive/20 hover:shadow-lg transition">
					<h3 class="text-xl font-bold text-brand-olive mb-3">{achievement.title}</h3>
					<p class="text-brand-dark leading-relaxed">{achievement.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>
