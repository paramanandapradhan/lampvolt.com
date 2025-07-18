<script lang="ts">
	import ConstactMap from '$lib/contact/components/constact-map.svelte';
	import ContactBanner from '$lib/contact/components/contact-banner.svelte';
	import ContactForm from '$lib/contact/components/contact-form.svelte';
	import AppNavbar from '$lib/core/components/app-navbar.svelte';
	import CopyRights from '$lib/core/components/copy-rights.svelte';
	import Footer from '$lib/core/components/footer.svelte';
</script>

<div class="min-h-full">
	<AppNavbar hasLogo />
	<div>
		<ContactBanner />
	</div>
	<div>
		<ContactForm />
	</div>
	<div>
		<ConstactMap />
	</div>
	<div>
		<Footer />
	</div>
	<div>
		<CopyRights />
	</div>
</div>
