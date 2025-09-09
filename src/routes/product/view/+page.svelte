<script lang="ts">
	import { page } from '$app/state';
	import AppNavbar from '$lib/core/components/app-navbar.svelte';

	import Footer from '$lib/core/components/footer.svelte';
	import CopyRights from '$lib/core/components/copy-rights.svelte';
	import ProductView from '$lib/products/components/product-view.svelte';
	import { goBack } from '@cloudparker/moldex.js';

	let productId = $derived(page.url.searchParams.get('productId'));
</script>

<div class="min-h-screen">
	<AppNavbar hasLogo hasBack onBack={goBack} />
	<div>
		<ProductView {productId} />
	</div>
	<div>
		<Footer />
	</div>
	<div>
		<CopyRights />
	</div>
</div>
