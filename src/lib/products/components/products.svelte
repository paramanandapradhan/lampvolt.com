<script lang="ts">
	import ProductCard from '$lib/common/components/product-card.svelte';
	import { products } from '../service';
	
</script>

<div class="relative flex min-h-screen items-center justify-center p-4 sm:p-6 lg:p-8">
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
		<h2 class="mb-8 text-4xl font-bold text-base-200">Featured Brands</h2>
		<div class="grid grid-cols-1 gap-4 sm:grid-cols-2 sm:gap-6 md:grid-cols-3 lg:grid-cols-4">
			{#each products as product}
				<div class="mb-4 w-full">
					<ProductCard>
						<div>
							<img src={product.images[0]} alt={product.title} class="h-auto w-full object-cover" />
							<h1 class="mt-2 text-center text-lg font-bold">{product.price}</h1>
						</div>
						<div>
							<h2 class="mb-2 text-lg font-bold">{product.title}</h2>
							<ul class="list-disc pl-2">
								{#each product.importantPoints as point}
									<li class="mb-1 text-xs">{point}</li>
								{/each}
							</ul>
							<div class="mt-8 mb-4 text-center">
								<a
									href={`/product/view?productId=${product.id}`}
									class="rounded bg-primary-500 px-4 py-2 text-white hover:bg-primary-600"
									>View Details</a
								>
							</div>
						</div>
					</ProductCard>
				</div>
			{/each}
		</div>
	</div>
</div>
