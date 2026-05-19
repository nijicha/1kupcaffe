<script lang="ts">
	import Sparkle from './decorations/Sparkle.svelte';
	import ArchLines from './decorations/ArchLines.svelte';
</script>

<section
	id="hero"
	class="relative min-h-screen bg-gradient-to-br from-brand-olive to-brand-olive flex flex-col items-center justify-center overflow-hidden"
>
	<!-- Background decorations -->
	<div class="absolute top-10 left-10 opacity-30">
		<Sparkle size="lg" color="#c8d9be" />
	</div>
	<div class="absolute bottom-20 right-10 opacity-20">
		<ArchLines count={4} opacity={0.3} />
	</div>

	<!-- Main content -->
	<div class="relative z-10 text-center px-4 max-w-4xl">
		<!-- Logo Badge SVG -->
		<div class="mb-8">
			<svg viewBox="0 0 200 200" class="w-40 h-40 mx-auto mb-6" xmlns="http://www.w3.org/2000/svg">
				<!-- Outer circle -->
				<circle cx="100" cy="100" r="95" fill="none" stroke="#c8d9be" stroke-width="2" />

				<!-- Circular text path -->
				<defs>
					<path
						id="textPath"
						d="M 100,100 m -75,0 a 75,75 0 1,1 150,0 a 75,75 0 1,1 -150,0"
						fill="none"
					/>
				</defs>
				<text
					font-size="10"
					font-weight="bold"
					fill="#c8d9be"
					letter-spacing="2"
					text-anchor="middle"
				>
					<textPath href="#textPath" startOffset="0%">· 1KUP CAFFE · EST. 2022 ·</textPath>
				</text>

				<!-- Coffee cup body -->
				<rect x="82" y="105" width="36" height="28" rx="2" fill="#c8d9be" />
				<!-- Cup handle -->
				<path
					d="M 118,112 Q 132,112 132,120 Q 132,128 118,128"
					fill="none"
					stroke="#c8d9be"
					stroke-width="3"
					stroke-linecap="round"
				/>
				<!-- Angel wings -->
				<g fill="#c8d9be" opacity="0.9">
					<path d="M 55,115 Q 35,85 65,95 Q 50,70 75,105 Z" />
					<path d="M 145,115 Q 165,85 135,95 Q 150,70 125,105 Z" />
				</g>

				<!-- Steaming lines -->
				<g stroke="#c8d9be" stroke-width="2" stroke-linecap="round" fill="none" opacity="0.7">
					<path d="M 88,103 Q 86,95 88,87" />
					<path d="M 100,101 Q 98,93 100,85" />
					<path d="M 112,103 Q 110,95 112,87" />
				</g>
			</svg>
		</div>

		<!-- Brand Name -->
		<h1 class="text-7xl md:text-8xl font-black text-brand-cream mb-4 tracking-tight">1KUP CAFFE</h1>

		<!-- Tagline -->
		<p class="text-2xl md:text-3xl font-bold text-brand-sage-light tracking-widest mb-12">
			FROM FARM TO CUP
		</p>

		<!-- Scroll indicator -->
		<div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
			<svg class="w-6 h-6 text-brand-sage-light" fill="none" stroke="currentColor" viewBox="0 0 24 24">
				<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
			</svg>
		</div>
	</div>
</section>
