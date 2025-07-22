<script lang="ts">
	import ContactCard from './contact-card.svelte';
</script>

<div class="relative min-h-screen">
	<!-- Background Image -->
	<div
		class="absolute inset-0 -z-10 w-full bg-cover bg-center"
		style="background-image: url(/imgs/contact-bg-1.webp);"
	></div>

	<div class="relative inset-0 h-full w-full items-center px-4 md:px-16 lg:px-32">
		<!-- Heading Section -->
		<div class="pt-24 text-center md:pt-32">
			<h4 class="text-primary-500 text-lg font-medium uppercase tracking-widest">Contact Us</h4>
			<h1 class="my-4 text-2xl font-black leading-tight text-white md:my-6 md:text-4xl">
				Get In Touch With an <br /> Expert
			</h1>
		</div>

		<!-- Contact Card -->
		<div class="w-full py-12 md:py-16">
			<ContactCard />
		</div>
	</div>
</div>
