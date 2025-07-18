<script lang="ts">
	import { onMount } from 'svelte';
	import { gsap } from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';

	// Register ScrollTrigger plugin
	gsap.registerPlugin(ScrollTrigger);

	const testimonials = [
		{
			img: 'avatar.svg',
			name: 'Amit Sharma',
			position: 'Farmer',
			text: '"The Tulu pump we purchased is a game-changer for our irrigation needs. Reliable, efficient, and built to last. Highly recommend this company!"'
		},
		{
			img: 'avatar.svg',
			name: 'Priya Patel',
			position: 'Agricultural Consultant',
			text: '"Their submersible pump exceeded our expectations. Seamless installation and outstanding performance. Truly a professional team!"'
		},
		{
			img: 'avatar.svg',
			name: 'Rohan Gupta',
			position: 'Water Management Engineer',
			text: '"The jet pump design is flawless, and the after-sales support is exceptional. A trusted partner for all our water solutions!"'
		},
		{
			img: 'avatar.svg',
			name: 'Sneha Reddy',
			position: 'Farm Owner',
			text: '"Top-quality motors and excellent service. The Tulu pump transformed our water supply system. Highly recommend their products!"'
		}
	];

	onMount(() => {
		// Animation for h1 (Customer Testimonials) - down to up
		gsap.from('.testimonial-heading', {
			opacity: 0,
			y: 50,
			duration: 1.2,
			ease: 'power3.out',
			scrollTrigger: {
				trigger: '.testimonial-heading',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});

		// Animation for testimonial cards - left to right one by one
		gsap.from('.testimonial-card', {
			opacity: 0,
			x: -100,
			duration: 1.2,
			ease: 'power3.out',
			stagger: 0.3,
			scrollTrigger: {
				trigger: '.testimonial-grid',
				start: 'top 80%',
				toggleActions: 'play none none none'
			}
		});
	});
</script>

<div class="mx-4 mt-12 lg:mt-32 min-h-screen md:mx-16">
	<h1 class="testimonial-heading mb-10 text-3xl font-bold text-base-200 sm:text-4xl">Customer Testimonials</h1>

	<div class="testimonial-grid grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
		{#each testimonials as testimonial, index}
			<div
				class="testimonial-card relative box-border flex w-full flex-col overflow-hidden rounded-xl bg-white shadow-lg"
			>
				<div class="flex items-center gap-4 p-6">
					<img
						src={testimonial.img}
						class="h-16 w-16 rounded-full object-cover ring-2 ring-blue-200"
						alt="{testimonial.name}'s Photo"
					/>
					<div>
						<h6 class="text-lg font-semibold text-gray-800">{testimonial.name}</h6>
						<p class="text-sm text-gray-500">{testimonial.position}</p>
					</div>
				</div>
				<div class="flex-1 bg-gray-50 p-6">
					<p class="italic text-gray-600">{testimonial.text}</p>
				</div>
				<div class="absolute right-4 top-4 h-3 w-3 rounded-full bg-primary-500"></div>
			</div>
		{/each}
	</div>
</div>

<style>
	.testimonial-grid {
		display: grid;
		grid-template-columns: repeat(1, minmax(0, 1fr));
		gap: 2rem;
	}

	@media (min-width: 640px) {
		.testimonial-grid {
			grid-template-columns: repeat(2, minmax(0, 1fr));
		}
	}

	@media (min-width: 1024px) {
		.testimonial-grid {
			grid-template-columns: repeat(4, minmax(0, 1fr));
		}
	}

	.testimonial-card {
		min-width: 0;
	}
</style>