<script lang="ts">
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		// Animate heading
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

		// Animate each card
		gsap.utils.toArray<HTMLElement>('.product-card').forEach((card, index) => {
			const xDirection = index % 2 === 0 ? -100 : 100;
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

		// Animate CTA
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

		// Hover video play/pause
		gsap.utils.toArray<HTMLElement>('.product-card').forEach((card) => {
			const video = card.querySelector('video');
			if (video) {
				card.addEventListener('mouseenter', () => {
					video.play();
				});
				card.addEventListener('mouseleave', () => {
					video.pause();
				});
			}
		});
	});
</script>

<div class="min-h-screen bg-base-900 px-4 py-12 sm:px-8 md:px-16 lg:px-32">
	<h1 class="product-heading mb-10 text-4xl font-extrabold text-base-200">
		Explore Our Collection
	</h1>

	<div class="grid grid-cols-1 items-stretch gap-4 lg:grid-cols-2">
		{#each [{ img: '/imgs/about-img.webp', video: '/video/home-video5.mp4', price: '₹ 9999', title: 'Motor Sensor Advanced Model 3 Phase Motor', name: 'LAV Advanced Model', features: ['Microcontroller Base: Yes', 'Low Voltage Protection: Yes', 'High Voltage Protection: Yes', 'Dry Run Protection: Yes', 'Digital Display: Yes', 'Warranty: 1 Year'] }, { img: '/imgs/product5.webp', video: '/video/home-video6.mp4', price: '₹ 5999', title: 'Motor Sensor Transister Base', name: 'LAV Basic Model', features: ['Microcontroller Base: No', 'Max Wire Length: 80M', 'Low Voltage Protection: Yes', 'Auto Mode: Yes', 'Manual Mode: Yes', 'Warranty: 1 Year'] }, { img: '/imgs/product2.webp', video: '/video/home-video7.mp4', price: '₹ 6499', title: 'Motor Sensor Supply Water', name: 'LAV Supply Water Model', features: ['Microcontroller Base: Yes', 'Body Type: Iron', 'HP: Up to 1.5 HP', 'Sump Protection: Yes', 'Low Voltage Protection: Yes', 'Digital Display: Yes', 'Warranty: 1 Year'] }, { img: '/imgs/about-img.webp', video: '/video/home-video8.mp4', price: '₹ 6999', title: 'Motor Sensor Advanced Model', name: 'LAV Advanced Model', features: ['Motor Model Support: Tulu, JET', 'High Voltage Protection: Yes', 'Dry Run Protection: Yes', 'Max Wire Length: 80M', 'Warranty: 1 Years'] }] as product}
			<div
				class="product-card flex flex-col rounded-xl bg-gray-800 bg-opacity-90 text-base-200 shadow-xl backdrop-blur-sm"
			>
				<!-- Top Section -->
				<div class="mt-2">
					<img src={product.img} alt="product" class="h-auto w-full rounded-t-xl object-cover" />
					<h1 class="mt-2 text-center text-lg font-bold">{product.price}</h1>
				</div>

				<!-- Bottom Section -->
				<div
					class="video-overlay group relative flex min-h-[400px] flex-grow flex-col justify-between overflow-hidden px-6 py-6 md:px-10 md:py-10 lg:px-16 lg:py-16"
				>
					<!-- Background Video -->
					<video
						class="absolute inset-0 z-0 h-full w-full object-cover transition-opacity duration-300"
						muted
						loop
						playsinline
						data-video
					>
						<source src={product.video} type="video/mp4" />
					</video>

					<!-- Text Content -->
					<div class="relative z-10">
						<h2 class="mb-2 text-lg font-bold">{product.title}</h2>
						<div class="mb-1 text-sm">
							<span class="font-semibold text-base-400">NAME OF PRODUCT: </span>
							<span class="font-bold text-base-300">{product.name}</span>
						</div>
						<ul class="mt-2 list-inside list-disc text-sm text-base-300">
							{#each product.features as feature}
								<li>{feature}</li>
							{/each}
						</ul>
					</div>
				</div>
			</div>
		{/each}
	</div>

	<!-- CTA -->
	<div class="shop-now mt-10 flex justify-center">
		<a
			href="/product"
			class="rounded-lg bg-primary-600 px-6 py-2 font-semibold text-white transition duration-300 hover:bg-primary-700"
		>
			Shop Now
		</a>
	</div>
</div>

<style>
	video[data-video] {
		pointer-events: none;
		filter: brightness(0.3) blur(2px); 
	}

	.video-overlay::after {
		content: '';
		position: absolute;
		inset: 0;
		background: rgba(0, 0, 0, 0.126); 
		z-index: 1;
		pointer-events: none;
	}
</style>
