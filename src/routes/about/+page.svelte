<script lang="ts">
	import HeroSection from '$lib/about/components/hero-section.svelte';
	import OurMission from '$lib/about/components/our-mission.svelte';
	import AppNavbar from '$lib/core/components/app-navbar.svelte';
	import CopyRights from '$lib/core/components/copy-rights.svelte';
	import Footer from '$lib/core/components/footer.svelte';
</script>

<div class="min-h-full">
	<AppNavbar hasLogo />
	<div>
		<HeroSection />
	</div>
    <div>
        <OurMission />
    </div>
	<div >
		<Footer />
	</div>
	<div>
		<CopyRights />
	</div>
</div>
