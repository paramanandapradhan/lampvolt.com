<script lang="ts">
	import TestimonialCard from '$lib/common/components/testimonial-card.svelte';
	import AppNavbar from '$lib/core/components/app-navbar.svelte';
	import CopyRights from '$lib/core/components/copy-rights.svelte';
	import Footer from '$lib/core/components/footer.svelte';
	import HeroSection from '$lib/home/components/hero-section.svelte';
	import HomeProductShowcase from '$lib/home/components/home-product-showcase.svelte';
	import NumberSection from '$lib/home/components/number-section.svelte';
	import OurStory from '$lib/home/components/our-story.svelte';
</script>

<div class="min-h-full">
	<AppNavbar hasLogo />

	<div>
		<HeroSection />
	</div>
	<div>
		<OurStory />
	</div>
	<div>
		<HomeProductShowcase />
	</div>
	<div>
		<NumberSection />
	</div>
	<div>
		<TestimonialCard />
	</div>
	<div>
		<Footer />
	</div>
	<div>
		<CopyRights />
	</div>
</div>
