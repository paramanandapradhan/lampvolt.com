<script lang="ts">
	import ProductCard from '$lib/common/components/product-card.svelte';
</script>

<div class="mx-4 my-6 min-h-screen sm:mx-8 md:mx-16 md:my-12 lg:mx-32">
	<h2 class="mb-8 text-4xl font-bold text-base-200">Featured Brands</h2>
	<div
		class="mb-6 grid grid-cols-1 gap-4 sm:mb-8 sm:grid-cols-2 sm:gap-6 md:grid-cols-3 lg:grid-cols-4"
	>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/product1.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 2999</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Base Model</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Basic Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV2</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">80M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 1.5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Palstic</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Tulu, JET</span>
					</div>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/about-img.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 6999</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Advanced Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV02</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">80M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 1.5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Tulu, JET</span>
					</div>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/about-img.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 7499</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Advanced Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV06</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">80M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 1.5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Submersible Pump</span>
					</div>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/about-img.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 7999</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Advanced Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV04</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">80M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 1.5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Submersible Pump</span>
					</div>
				</div>
			</ProductCard>
		</div>
	</div>
	<div
		class="mb-6 grid grid-cols-1 gap-4 sm:mb-8 sm:grid-cols-2 sm:gap-6 md:grid-cols-3 lg:grid-cols-4"
	>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/about-img.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 8999</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model 3 Phase Motor</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Advanced Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV04</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">150M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Submersible Pump</span>
					</div>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/about-img.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 9999</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model 3 Phase Motor</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Advanced Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV04</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">200M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Submersible Pump</span>
					</div>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/product5.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 5999</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Transister Base</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Basic Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV02</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">80M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 1.5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">No</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Submersible Pump</span>
					</div>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/product2.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 6499</h1>
				</div>
				<div>
					<h2 class="mb-2 text-lg font-bold">Motor Sensor Supply Water</h2>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">NAME OF PRODUCT :- </span>
						<span class="font-bold text-base-300">LAV Supply Water Model</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MODEL NAME :- </span>
						<span class="font-bold text-base-300">LAV02s</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MICROCONTROLLER BASE :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MAX WIRE LENGTH WORKS :- </span>
						<span class="font-bold text-base-300">80M</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HP :- </span>
						<span class="font-bold text-base-300">UPTO 1.5HP</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">BODY TYPE :- </span>
						<span class="font-bold text-base-300">Iron</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">LO VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">HI VOLTAGE PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DRY RUN PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">AUTO :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MANUAL :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">SUMP PROTECTION :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">DIGITAL DISPLAY :- </span>
						<span class="font-bold text-base-300">Yes</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">WARRANTY :- </span>
						<span class="font-bold text-base-300">1 Year</span>
					</div>
					<div class="mb-1 text-sm">
						<span class="font-semibold text-base-400">MOTOR MODEL SUPPORT :- </span>
						<span class="font-bold text-base-300">Supply Water</span>
					</div>
				</div>
			</ProductCard>
		</div>
	</div>
	<div class="grid grid-cols-1 gap-4 sm:grid-cols-2 sm:gap-6 md:grid-cols-3 lg:grid-cols-4">
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/product4.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 3499</h1>
				</div>
				<div>
					<h2 class="text-lg font-bold">Home Automation IR Base</h2>
				</div>
			</ProductCard>
		</div>
		<div class="mb-4 w-full">
			<ProductCard>
				<div>
					<img src="/imgs/product3.webp" alt="product" class="h-auto w-full object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">₹ 6999</h1>
				</div>
				<div>
					<h2 class="text-lg font-bold">Home Automation Wifi Base</h2>
				</div>
			</ProductCard>
		</div>
	</div>
</div>
