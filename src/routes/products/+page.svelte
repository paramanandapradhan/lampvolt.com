<script lang="ts">
	import AppNavbar from '$lib/core/components/app-navbar.svelte';
	import CopyRights from '$lib/core/components/copy-rights.svelte';
	import Footer from '$lib/core/components/footer.svelte';
	import Faq from '$lib/faq/faq.svelte';
	import Categories from '$lib/products/components/categories.svelte';
	import Products from '$lib/products/components/products.svelte';
</script>

<div class="min-h-full">
	<AppNavbar hasLogo />
	<div>
		<Categories />
	</div>
	<div>
		<Products />
	</div>
	<div id="faq">
		<Faq />
	</div>
	<div>
		<Footer />
	</div>
	<div>
		<CopyRights />
	</div>
</div>
