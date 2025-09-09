<script lang="ts">
	import { Button } from '@cloudparker/moldex.js';

	import { mdiChevronLeft, mdiChevronRight } from '$lib/core/services/app-icons-service.js';
	import { products } from '../service';

	

	type Props = {
		productId?: string | null;
	};

	let { productId }: Props = $props();

	let product = $derived(products.find((p) => p.id === productId));

	let currentImageIndex = $state(0);

	$effect(() => {
		if (product) {
			currentImageIndex = Math.max(0, Math.min(currentImageIndex, product.images.length - 1));
		}
	});

	function nextImage() {
		if (product && product.images.length > 1) {
			currentImageIndex = (currentImageIndex + 1) % product.images.length;
		}
	}

	function prevImage() {
		if (product && product.images.length > 1) {
			currentImageIndex = (currentImageIndex - 1 + product.images.length) % product.images.length;
		}
	}

	function goToImage(index: number) {
		if (product) {
			currentImageIndex = index;
		}
	}
</script>

<div class="relative flex min-h-screen items-center justify-center">
	<div
		aria-hidden="true"
		class="absolute inset-x-0 top-0 -z-10 -translate-y-1/2 transform-gpu overflow-hidden opacity-30 blur-3xl"
	>
		<div
			style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"
			class="ml-[max(50%,38rem)] aspect-[1313/771] w-[82.0625rem] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc]"
		></div>
	</div>
	<div
		aria-hidden="true"
		class="absolute inset-x-0 top-1/2 -z-10 flex transform-gpu overflow-hidden pt-32 opacity-10 blur-3xl sm:pt-40 xl:justify-end"
	>
		<div
			style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)"
			class="ml-[-22rem] aspect-[1313/771] w-[82.0625rem] flex-none origin-top-right rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] xl:ml-0 xl:mr-[calc(50%-12rem)]"
		></div>
	</div>
	<div class="mx-auto w-full max-w-7xl text-white">
		{#if product}
			<div class="mx-4 my-6 sm:mx-8 md:mx-16 md:my-12 lg:mx-32">
				<h1 class="mb-4 text-4xl font-bold text-base-200">{product.title}</h1>
				

				<!-- Image Carousel -->
				<div class="relative mb-8">
					<div class="relative px-0 lg:px-32">
						<img
							src={product.images[currentImageIndex]}
							alt={`${product.title} - Image ${currentImageIndex + 1} of ${product.images.length}`}
							class="h-auto max-h-[500px] w-full rounded-md object-contain shadow-md sm:max-h-[600px]"
						/>
						{#if product.images.length > 1}
							<div class="absolute inset-y-0 left-0 flex items-center">
								<Button onClick={prevImage} iconPath={mdiChevronLeft} />
							</div>
							<div class="absolute inset-y-0 right-0 flex items-center">
								<Button onClick={nextImage} iconPath={mdiChevronRight} />
							</div>
							<div class="mt-4 flex justify-center space-x-2">
								{#each product.images as _, index}
									<button
										onclick={() => goToImage(index)}
										aria-label={`Go to image ${index + 1}`}
										class="h-3 w-3 rounded-full focus:outline-none focus:ring-2 focus:ring-blue-500 {currentImageIndex ===
										index
											? 'bg-blue-500'
											: 'bg-gray-300'}"
									></button>
								{/each}
							</div>
						{/if}
					</div>
				</div>

                <div class="mb-4  text-2xl font-bold text-base-200">
					<span>Price: </span>{product.price}
				</div>
				<!-- Important Points -->
				<div class="mb-6">
					<h2 class="mb-4 text-2xl font-bold text-base-200">Key Features</h2>
					<ul class="list-disc space-y-1 pl-5">
						{#each product.importantPoints as point}
							<li class="text-base-300">{point}</li>
						{/each}
					</ul>
				</div>

				<!-- Product Details -->
				{#if Object.keys(product.details).length > 0}
					<div class="mb-6">
						<h2 class="mb-4 text-2xl font-bold text-base-200">Full Specifications</h2>
						<div class="grid grid-cols-1 gap-4 sm:grid-cols-2">
							{#each Object.entries(product.details) as [key, value]}
								<div class="text-sm">
									<span class="font-semibold text-base-400">{key}:</span>
									<span class="ml-1 font-bold text-base-300">{value}</span>
								</div>
							{/each}
						</div>
					</div>
				{/if}
			</div>
		{:else}
			<div class="mx-4 my-6">
				<h1 class="text-2xl font-bold text-base-200">Product Not Found</h1>
				<p class="text-base-300">The requested product does not exist.</p>
				<a href="/products" class="text-blue-500 underline">Back to Products</a>
			</div>
		{/if}
	</div>
</div>
