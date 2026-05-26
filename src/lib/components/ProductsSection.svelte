<script lang="ts">
	const products = [
		{
			category: 'Physical Products',
			items: [
				{
					title: 'Traceable Green Coffee',
					desc: 'SCA 82–86 lots from Thailand, Myanmar (Shan), and Laos; microlots and commercial grades; 60–69 kg GrainPro-in-jute.',
				},
				{
					title: 'Private-Label RTD Coffee',
					desc: 'Cans/bottles; recipe development and co-pack coordination.',
				},
			],
		},
		{
			category: 'Digital Products',
			items: [
				{
					title: 'Farmer AI App',
					desc: 'Offline-first: Ripeness/defect detection, drying coach, yield forecasts; Burmese/Shan/Thai/Lao.',
				},
				{
					title: 'Buyer Dashboard + TraceChain API',
					desc: 'Lot-level traceability, QC data, compliance packs (photo/ICO/COO), ERP integration.',
				},
				{
					title: 'QC Vision',
					desc: 'Camera-based defect and moisture workflow for mills/warehouses.',
				},
			],
		},
		{
			category: 'Bundles (Productized Services)',
			items: [
				{
					title: 'Origin-to-FOB Package',
					desc: 'Sourcing, QC, documentation, and export.',
				},
				{
					title: 'Cross-Border Distribution Package',
					desc: 'Customs, 3PL warehousing, and last-mile in ASEAN.',
				},
			],
		},
	];
</script>

<section id="products" class="py-24 px-4 bg-white">
	<div class="max-w-7xl mx-auto">
		<h2 class="text-5xl md:text-6xl font-bold text-brand-olive mb-16">Our Products</h2>

		<div class="space-y-20">
			{#each products as productGroup}
				<div>
					<h3 class="text-3xl font-bold text-brand-olive mb-8">{productGroup.category}</h3>
					<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
						{#each productGroup.items as product}
							<div class="bg-white border-2 border-brand-sage-light rounded-lg p-8 hover:shadow-lg transition">
								<div class="h-32 bg-gradient-to-br from-brand-olive to-brand-sage rounded-lg mb-6"></div>
								<h4 class="text-xl font-bold text-brand-dark mb-3">{product.title}</h4>
								<p class="text-brand-dark/80 leading-relaxed">{product.desc}</p>
							</div>
						{/each}
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
