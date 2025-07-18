<script lang="ts">
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		// Removed parallax effect

		gsap.from('.mission-heading', {
			opacity: 0,
			y: 50,
			duration: 1,
			scrollTrigger: {
				trigger: '.mission-heading',
				start: 'top 80%'
			}
		});

		gsap.from('.core-values h1', {
			opacity: 0,
			y: 50,
			duration: 1,
			scrollTrigger: {
				trigger: '.core-values h1',
				start: 'top 80%'
			}
		});

		gsap.utils.toArray('.core-values .value-item').forEach((item: any, index) => {
			gsap.from(item, {
				opacity: 0,
				y: 50,
				duration: 1,
				delay: index * 0.2,
				scrollTrigger: {
					trigger: item,
					start: 'top 80%'
				}
			});
		});

		gsap.from('.first-paragraph', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.first-paragraph',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});

		gsap.from('.second-paragraph-mission', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.second-paragraph-mission',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});
	});
</script>

<!-- Background Image Section -->
<div class="relative z-0 w-full">
	<div
		class="px-4 py-16 md:px-16 lg:px-32 text-white bg-cover bg-center bg-no-repeat"
		style="
			background-image: url('imgs/about-background.avif');
			background-size: 120% 120%;
			background-blend-mode: multiply;
			background-color: rgba(0,0,0,0.7);
		"
	>
		<!-- Our Mission -->
		<h1 class="mission-heading mb-12 text-4xl font-extrabold">
			Our Mission
		</h1>

		<div class="mb-6 md:mb-12 lg:mb-16">
			<div class="grid grid-cols-12 gap-6">
				<div class="col-span-12 lg:col-span-10">
					<p class="mb-4 text-lg leading-relaxed font-bold first-paragraph">
						At LAmpVolt, our mission is to empower customers with innovative, intuitive products
						that seamlessly integrate into their daily lives. We strive to deliver solutions that
						not only meet the demands of modern homes and farms but also anticipate future needs,
						fostering a balance between technology and sustainability.
					</p>
					<p class="text-lg leading-relaxed text-base-400 second-paragraph-mission">
						We aim to enhance productivity and convenience while minimizing environmental impact for
						smarter, greener living.
					</p>
				</div>
			</div>
		</div>

		<!-- Core Values -->
		<div class="core-values">
			<h1 class="mb-4 lg:mb-10 inline-block rounded bg-opacity-80 p-2 text-2xl font-bold text-white">
				Core Values
			</h1>

			<div class="grid grid-cols-1 lg:grid-cols-3 gap-6 rounded-lg bg-gray-900 bg-opacity-90 px-6 py-6 md:py-10 lg:py-20 shadow-md">
				<!-- Value 1 -->
				<div class="value-item">
					<div class="mb-6 flex justify-start items-center gap-6">
						<div class="h-12 w-2 rounded bg-primary-600"></div>
						<h2 class="mb-2 text-xl font-semibold text-white">Innovation</h2>
					</div>
					<p class="text-sm text-base-300 text-start">
						We drive groundbreaking ideas, exploring new technologies to redefine convenience and
						efficiency for homes and farms.
					</p>
				</div>

				<!-- Value 2 -->
				<div class="value-item">
					<div class="mb-6 flex justify-start items-center gap-6">
						<div class="h-12 w-2 rounded bg-primary-600"></div>
						<h2 class="mb-2 text-xl font-semibold text-white">Transparency</h2>
					</div>
					<p class="text-sm text-base-300 text-start">
						We build trust through open communication, ensuring quality and integrity in our
						manufacturing and designs.
					</p>
				</div>

				<!-- Value 3 -->
				<div class="value-item">
					<div class="mb-6 flex justify-start items-center gap-6">
						<div class="h-12 w-2 rounded bg-primary-600"></div>
						<h2 class="mb-2 text-xl font-semibold text-white">Accessibility</h2>
					</div>
					<p class="text-sm text-base-300 text-start">
						We craft intuitive, inclusive products, making advanced technology accessible to all for
						modern living and farming.
					</p>
				</div>
			</div>
		</div>

		
	</div>
</div>
