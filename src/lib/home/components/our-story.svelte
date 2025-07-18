<script lang="ts">
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';

	// Register ScrollTrigger plugin
	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		// Animation for h1 (Our Story) when it enters viewport
		gsap.from('.heading', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.heading',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});

		// Animation for first paragraph and image when they enter viewport
		gsap.from('.initial-content', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.initial-content',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});

		// Animation for second paragraph when it enters viewport
		gsap.from('.second-paragraph-hero', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.second-paragraph-hero',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});
	});
</script>

<div class="mx-auto my-12 px-4 sm:px-6 lg:px-32 min-h-screen">
	<h1 class="heading mb-8 sm:mb-10 text-3xl sm:text-4xl font-extrabold text-base-200">Our Story</h1>
	<div
		class="max-w-full rounded-xl bg-gray-800 bg-opacity-90 px-4 py-6 text-base-200 shadow-xl backdrop-blur-sm sm:px-6 sm:py-8 md:px-10 md:py-10 lg:px-16 lg:py-16"
	>
		<div class="grid grid-cols-1 md:grid-cols-2 items-center gap-6 md:gap-8">
			<div>
				<p
					class="initial-content mb-8 md:mb-12 text-lg sm:text-xl font-bold leading-relaxed tracking-wide text-base-300"
				>
					Welcome to LAmpVolt, where innovation meets everyday life. Founded in 2015 with a vision
					to enrich homes and farms with cutting-edge technology, we have established ourselves as a
					pioneering manufacturer of electronic-based home appliances and agricultural products.
				</p>

				<div class="second-paragraph-hero">
					<a
						href="/about"
						class="block lg:inline-block w-full lg:w-auto rounded-lg bg-primary-600 px-4 py-2 sm:px-6 sm:py-2 font-semibold text-white transition duration-300 hover:bg-primary-700 text-center"
					>
						Read More
					</a>
				</div>
			</div>
			<div class="initial-content">
				<img
					src="/imgs/about-img.webp"
					alt="who we are"
					class="h-auto w-full transform rounded-lg shadow-2xl transition-transform duration-300 hover:scale-105"
				/>
			</div>
		</div>
	</div>
</div>