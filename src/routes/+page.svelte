<script lang="ts">
	import Nav from '$lib/components/Nav.svelte';
	import HeroSection from '$lib/components/HeroSection.svelte';
	import AboutSection from '$lib/components/AboutSection.svelte';
	import VisionMissionSection from '$lib/components/VisionMissionSection.svelte';
	import ServicesSection from '$lib/components/ServicesSection.svelte';
	import ProductsSection from '$lib/components/ProductsSection.svelte';
	import TargetMarketSection from '$lib/components/TargetMarketSection.svelte';
	import AchievementsSection from '$lib/components/AchievementsSection.svelte';
	import FuturePlansSection from '$lib/components/FuturePlansSection.svelte';
	import ContactFooter from '$lib/components/ContactFooter.svelte';
</script>

<Nav />

<main>
	<HeroSection />
	<AboutSection />
	<VisionMissionSection />
	<ServicesSection />
	<ProductsSection />
	<TargetMarketSection />
	<AchievementsSection />
	<FuturePlansSection />
</main>

<ContactFooter />
