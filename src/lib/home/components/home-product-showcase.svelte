<script lang="ts">
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';

	// Register ScrollTrigger plugin
	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		// Animation for h1 (Explore Our Collection) - down to up
		gsap.from('.product-heading', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.product-heading',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});

		// Animation for grid items - alternating left to right and right to left
		gsap.utils.toArray<HTMLElement>('.product-card').forEach((card, index) => {
			const xDirection = index % 2 === 0 ? -100 : 100; // Even index: left to right, Odd index: right to left
			gsap.from(card, {
				opacity: 0,
				x: xDirection,
				duration: 1.2,
				ease: 'power3.out',
				scrollTrigger: {
					trigger: card,
					start: 'top 80%',
					toggleActions: 'play none none none'
				}
			});
		});

		// Animation for Shop Now button - down to up
		gsap.from('.shop-now', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.shop-now',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});
	});
</script>

<div class="min-h-screen bg-primary-100 px-4 py-12 sm:px-8 md:px-16 lg:px-32">
	<h1 class="product-heading mb-10 text-4xl font-extrabold text-base-800">
		Explore Our Collection
	</h1>
	<div class="grid grid-cols-1 gap-4 lg:grid-cols-2">
		<div class="product-card rounded-xl bg-gray-800 bg-opacity-90 text-base-200 shadow-xl backdrop-blur-sm">
			<div class="mt-2">
				<img
					src="/imgs/about-img.webp"
					alt="product 1"
					class="h-auto w-full rounded-t-xl object-cover"
				/>
				<h1 class="mt-2 text-center text-lg font-bold">₹ 9999</h1>
			</div>
			<div class="px-6 py-6 md:px-10 md:py-10 lg:px-16 lg:py-16">
				<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model 3 Phase Motor</h2>
				<div class="mb-1 text-sm">
					<span class="font-semibold text-base-400">NAME OF PRODUCT: </span>
					<span class="font-bold text-base-300">LAV Advanced Model</span>
				</div>
				<ul class="mt-2 list-inside list-disc text-sm text-base-300">
					<li>Microcontroller Base: Yes</li>
					<li>Low Voltage Protection: Yes</li>
					<li>High Voltage Protection: Yes</li>
					<li>Dry Run Protection: Yes</li>
					<li>Digital Display: Yes</li>
					<li>Warranty: 1 Year</li>
				</ul>
			</div>
		</div>
		<div class="product-card rounded-xl bg-gray-800 bg-opacity-90 text-base-200 shadow-xl backdrop-blur-sm">
			<div class="mt-2">
				<img
					src="/imgs/product5.webp"
					alt="product 2"
					class="h-auto w-full rounded-t-xl object-cover"
				/>
				<h1 class="mt-2 text-center text-lg font-bold">₹ 5999</h1>
			</div>
			<div class="px-6 py-6 md:px-10 md:py-10 lg:px-16 lg:py-16">
				<h2 class="mb-2 text-lg font-bold">Motor Sensor Transister Base</h2>
				<div class="mb-1 text-sm">
					<span class="font-semibold text-base-400">NAME OF PRODUCT: </span>
					<span class="font-bold text-base-300">LAV Basic Model</span>
				</div>
				<ul class="mt-2 list-inside list-disc text-sm text-base-300">
					<li>Microcontroller Base: No</li>
					<li>Max Wire Length: 80M</li>
					<li>Low Voltage Protection: Yes</li>
					<li>Auto Mode: Yes</li>
					<li>Manual Mode: Yes</li>
					<li>Warranty: 1 Year</li>
				</ul>
			</div>
		</div>
		<div class="product-card rounded-xl bg-gray-800 bg-opacity-90 text-base-200 shadow-xl backdrop-blur-sm">
			<div class="mt-2">
				<img
					src="/imgs/product2.webp"
					alt="product 3"
					class="h-auto w-full rounded-xl object-cover"
				/>
				<h1 class="mt-2 text-center text-lg font-bold">₹ 6499</h1>
			</div>
			<div class="px-6 py-6 md:px-10 md:py-10 lg:px-16 lg:py-16">
				<h2 class="mb-2 text-lg font-bold">Motor Sensor Supply Water</h2>
				<div class="mb-1 text-sm">
					<span class="font-semibold text-base-400">NAME OF PRODUCT: </span>
					<span class="font-bold text-base-300">LAV Supply Water Model</span>
				</div>
				<ul class="mt-2 list-inside list-disc text-sm text-base-300">
					<li>Microcontroller Base: Yes</li>
					<li>Body Type: Iron</li>
					<li>HP: Up to 1.5 HP</li>
					<li>Sump Protection: Yes</li>
					<li>Low Voltage Protection: Yes</li>
					<li>Digital Display: Yes</li>
					<li>Warranty: 1 Year</li>
				</ul>
			</div>
		</div>
		<div class="product-card rounded-xl bg-gray-800 bg-opacity-90 text-base-200 shadow-xl backdrop-blur-sm">
			<div class="mt-2">
				<img
					src="/imgs/about-img.webp"
					alt="product 4"
					class="h-auto w-full rounded-t-xl object-cover"
				/>
				<h1 class="mt-2 text-center text-lg font-bold">₹ 6999</h1>
			</div>
			<div class="px-6 py-6 md:px-10 md:py-10 lg:px-16 lg:py-16">
				<h2 class="mb-2 text-lg font-bold">Motor Sensor Advanced Model</h2>
				<div class="mb-1 text-sm">
					<span class="font-semibold text-base-400">NAME OF PRODUCT: </span>
					<span class="font-bold text-base-300">LAV Advanced Model</span>
				</div>
				<ul class="mt-2 list-inside list-disc text-sm text-base-300">
					<li>Motor Model Support: Tulu, JET</li>
					<li>High Voltage Protection: Yes</li>
					<li>Dry Run Protection: Yes</li>
					<li>Max Wire Length: 80M</li>
					<li>Warranty: 1 Years</li>
				</ul>
			</div>
		</div>
	</div>
	<div class=" shop-now mt-10 flex justify-center">
		<a
			href="/product"
			class="rounded-lg bg-primary-600 px-6 py-2 font-semibold text-white transition duration-300 hover:bg-primary-700"
		>
			Shop Now
		</a>
	</div>
</div>