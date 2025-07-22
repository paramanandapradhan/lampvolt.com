<script lang="ts">
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';

	gsap.registerPlugin(ScrollTrigger);

	onMount(() => {
		// Animation for heading
		gsap.from('.number-heading', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.number-heading',
				start: 'top 85%',
				toggleActions: 'play none none none'
			}
		});

		// Animation for numbers loading left to right
		gsap.from('.number', {
			opacity: 0,
			x: -50,
			stagger: 0.15,
			duration: 0.8,
			scrollTrigger: {
				trigger: '.numbers-container',
				start: 'top 85%',
				once: true
			}
		});

		// Parallax effect for background (less intense on mobile)
		gsap.fromTo(
			'.parallax-container',
			{ backgroundPositionX: '0%' },
			{
				backgroundPositionX: window.innerWidth < 640 ? '20%' : '50%', // Less movement on small screens
				ease: 'none',
				scrollTrigger: {
					trigger: '.numbers-container',
					start: 'top 100%',
					end: 'bottom 20%',
					scrub: true,
					markers: false
				}
			}
		);

		// Refresh ScrollTrigger on window resize to handle responsive changes
		const refreshScrollTrigger = () => {
			ScrollTrigger.refresh();
		};

		window.addEventListener('resize', refreshScrollTrigger);

		return () => {
			window.removeEventListener('resize', refreshScrollTrigger);
		};
	});
</script>

<div class="relative min-h-screen overflow-hidden text-white">
	<div
		class="parallax-container absolute inset-0 bg-cover bg-center"
		style="background-image: url('/imgs/home-image2.avif'); opacity: 0.7;"
	></div>
	<div class="numbers-container relative z-10 flex min-h-screen flex-col items-center justify-center lg:justify-start my-12 lg:my-32">
		<h1
			class="number-heading mb-24 text-center text-2xl font-bold text-base-200 sm:text-3xl md:text-4xl lg:text-5xl"
		>
			We Take Pride in Our Numbers
		</h1>
		<div
			class="mx-auto grid w-full max-w-7xl grid-cols-1 gap-6 px-4 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5"
		>
			<div class="number text-center">
				<div class="mb-2 text-3xl font-bold text-primary-600 sm:text-4xl md:text-5xl">10</div>
				<div class="mb-2 text-xs font-semibold text-base-400 sm:text-sm md:text-base">
					Years of Experience
				</div>
				<div class="mx-auto mt-2 w-2/3 rounded-full border-t-4 border-base-600"></div>
			</div>
			<div class="number text-center">
				<div class="mb-2 text-3xl font-bold text-primary-600 sm:text-4xl md:text-5xl">10</div>
				<div class="mb-2 text-xs font-semibold text-base-400 sm:text-sm md:text-base">
					Business Partners
				</div>
				<div class="mx-auto mt-2 w-2/3 rounded-full border-t-4 border-base-600"></div>
			</div>
			<div class="number text-center">
				<div class="mb-2 text-3xl font-bold text-primary-600 sm:text-4xl md:text-5xl">10K</div>
				<div class="mb-2 text-xs font-semibold text-base-400 sm:text-sm md:text-base">
					Products Installed
				</div>
				<div class="mx-auto mt-2 w-2/3 rounded-full border-t-4 border-base-600"></div>
			</div>
			<div class="number text-center">
				<div class="mb-2 text-3xl font-bold text-primary-600 sm:text-4xl md:text-5xl">1</div>
				<div class="mb-2 text-xs font-semibold text-base-400 sm:text-sm md:text-base">
					Countries World Wide
				</div>
				<div class="mx-auto mt-2 w-2/3 rounded-full border-t-4 border-base-600"></div>
			</div>
			<div class="number text-center">
				<div class="mb-2 text-3xl font-bold text-primary-600 sm:text-4xl md:text-5xl">1</div>
				<div class="mb-2 text-xs font-semibold text-base-400 sm:text-sm md:text-base">
					Industry Awards
				</div>
				<div class="mx-auto mt-2 w-2/3 rounded-full border-t-4 border-base-600"></div>
			</div>
		</div>
	</div>
</div>