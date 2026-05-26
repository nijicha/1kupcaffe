<script lang="ts">
	const services = [
		{
			id: 'core-coffee',
			title: 'Core Coffee Services',
			items: [
				'Origin sourcing (Thailand/Chiang Mai–Chiang Rai): Specialty arabica (Doi Chang/Doi Tung), washed/natural, SCA 82–85+, fast FOB Laem Chabang.',
				'Origin sourcing (Myanmar/Shan): Farm-to-FOB green coffee (Ywangan/Pyin Oo Lwin), SCA 82+, sanctions-screened partners; FOB Yangon or cross-border via Mae Sot.',
				'Origin sourcing (Laos/Bolaven Plateau): Premium arabica microlots/commercial grades, SCA 82–86, organic options; export via Thanaleng SEZ/Laem Chabang.',
				'Quality control: Cupping, moisture/WA testing, defect grading.',
				'Traceable lots: QR/lot IDs, farm/process/date records.',
				'Export management: Phyto/ICO/COO, customs, insurance.',
			],
		},
		{
			id: 'technology',
			title: 'Technology for Farmers/Partners',
			items: [
				'Offline-first AI app: Ripeness/defect detection, drying coach, yield forecasts. UI in Burmese, Shan, Thai, and Lao; works offline with low-end Android.',
				'Farm onboarding & data: Plot mapping, input logs, and SMS/push alerts in Burmese/Shan/Thai/Lao; supports forms in Myanmar, Thailand, and Laos.',
				'Lot management: Create/merge/split lots; assign QR/GSI IDs; capture process dates, moisture/WA, and cup scores; carton/pallet mapping for exports.',
				'Traceability & analytics: Buyer dashboard by lot/origin (TH/MM/LA), real-time status, compliance packs (ICO/photo/COO), and audit-ready reports.',
			],
		},
		{
			id: 'product-dev',
			title: 'Product Development',
			items: [
				'Coffee R&D: Processing protocols (washed/natural/honey), flavor profiling.',
				'RTD/soluble support: Recipe development, co-pack coordination.',
			],
		},
		{
			id: 'logistics',
			title: 'Logistics & Trade',
			items: [
				'Cross-border movement: Myanmar–Thailand–Laos–Vietnam–Malaysia–Singapore routing; air/sea via BKK, LCB, SGN, SIN; consolidation and FCL/LCL.',
				'Customs & brokerage: HS classification, ASEAN Single Window, FDA/food permits, phyto/ICO/COO, e-declarations, IOR/EOR.',
				'Multimodal transport: FTL/LTL, rail (China–Laos–Thailand), river where viable; cold/ambient options.',
				'Bonded/FTZ solutions: Duty deferment, bonded warehousing, transshipment, B2B cross-border e-commerce.',
				'Warehousing/fulfillment: Partner 3PLs in Bangkok/Laem Chabang, HCMC, Singapore; WMS, FEFO, kitting, rework, light QC.',
				'Inventory control: Batch/lot and QR/GSI tracking, cycle counts, VMI, safety-stock planning.',
			],
		},
		{
			id: 'advisory',
			title: 'Advisory & Training',
			items: [
				'Farmer training: Picking, sorting, drying, storage.',
				'Compliance setup: Sanctions/KYC, HACCP/FDA guidance, labeling.',
				'Market entry: Channel and distributor matchmaking in ASEAN.',
			],
		},
		{
			id: 'esg',
			title: 'ESG & Impact',
			items: [
				'Income uplift programs: Quality-premium schemes and instant payments.',
				'Circular practices: Waste reduction, by-product utilization.',
				'Impact reporting: Farmer metrics, traceability, emissions/waste.',
			],
		},
	];

	let activeTab = $state(0);
	let openItems = $state(new Set<number>());

	function toggleAccordion(index: number) {
		if (openItems.has(index)) {
			openItems.delete(index);
		} else {
			openItems.add(index);
		}
		openItems = openItems;
	}
</script>

<section id="services" class="py-24 px-4 bg-brand-cream">
	<div class="max-w-7xl mx-auto">
		<h2 class="text-5xl md:text-6xl font-bold text-brand-olive mb-16">Our Services</h2>

		<!-- Desktop: Tabs -->
		<div class="hidden md:block">
			<div class="flex flex-wrap gap-2 mb-8 border-b-2 border-brand-sage-light/30">
				{#each services as service, i}
					<button
						onclick={() => (activeTab = i)}
						class="px-4 py-3 font-semibold text-sm transition-colors {activeTab === i
							? 'bg-brand-olive text-brand-cream border-b-2 border-brand-olive'
							: 'text-brand-dark hover:bg-brand-sage-light/20'}"
					>
						{service.title}
					</button>
				{/each}
			</div>

			<!-- Tab Panel -->
			<div class="transition-opacity duration-300">
				<h3 class="text-2xl font-bold text-brand-olive mb-6">{services[activeTab].title}</h3>
				<ul class="space-y-4">
					{#each services[activeTab].items as item}
						<li class="flex gap-3">
							<span class="flex-shrink-0 text-brand-olive font-bold">•</span>
							<span class="text-brand-dark leading-relaxed">{item}</span>
						</li>
					{/each}
				</ul>
			</div>
		</div>

		<!-- Mobile: Accordion -->
		<div class="md:hidden space-y-2">
			{#each services as service, i}
				<div class="border border-brand-sage-light/30 rounded">
					<button
						onclick={() => toggleAccordion(i)}
						class="w-full px-6 py-4 flex justify-between items-center hover:bg-brand-sage-light/10 transition font-semibold text-brand-dark text-left"
					>
						<span>{service.title}</span>
						<svg
							class="w-5 h-5 transition-transform {openItems.has(i) ? 'rotate-180' : ''}"
							fill="none"
							stroke="currentColor"
							viewBox="0 0 24 24"
						>
							<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
						</svg>
					</button>
					{#if openItems.has(i)}
						<div class="px-6 py-4 bg-brand-cream border-t border-brand-sage-light/30 space-y-3">
							{#each service.items as item}
								<div class="flex gap-3">
									<span class="flex-shrink-0 text-brand-olive font-bold">•</span>
									<span class="text-brand-dark text-sm leading-relaxed">{item}</span>
								</div>
							{/each}
						</div>
					{/if}
				</div>
			{/each}
		</div>
	</div>
</section>
