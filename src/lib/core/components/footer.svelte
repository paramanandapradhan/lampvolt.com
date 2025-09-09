<script lang="ts">
	import { Icon } from '@cloudparker/moldex.js';
	import {
		mdiEmailOutline,
		mdiFacebook,
		mdiInstagram,
		mdiLinkedin,
		mdiPhone,
		mdiTwitter,
		mdiYoutube
	} from '../services/app-icons-service';
	import Newsletter from '$lib/common/components/newsletter.svelte';
</script>

<div class="mx-auto my-8 px-4 md:my-12 md:px-16 lg:my-32 ">
	<div
		class="text-base-200 grid grid-cols-1 gap-10 text-center md:grid-cols-2 lg:grid-cols-4 lg:text-left"
	>
		<div
			class="flex flex-col items-center justify-center space-y-6 lg:items-start lg:justify-start"
		>
			<div class="flex items-center gap-4">
				<a href="/">
					<img src="/lvt-logo2.svg" alt="logo" class=" !h-8 !w-auto !object-contain !filter !brightness-0 !invert" />
				</a>
				<!-- <h1 class="text-center font-black">Lampvolt</h1> -->
			</div>
			<div class="flex gap-3">
				<a
					href="https://www.facebook.com/HelloCallai"
					class="border-primary-600 hover:bg-primary-600 flex h-8 w-8 items-center justify-center rounded-full border-2 p-1 transition hover:text-white"
				>
					<Icon path={mdiFacebook} className="h-16 w-16" />
				</a>
				<a
					href="https://www.instagram.com/hellocall.ai/"
					class="border-primary-600 hover:bg-primary-600 flex h-8 w-8 items-center justify-center rounded-full border-2 p-1 transition hover:text-white"
				>
					<Icon path={mdiInstagram} className="h-16 w-16" />
				</a>
				<a
					href="https://x.com/hellocallai"
					class="border-primary-600 hover:bg-primary-600 flex h-8 w-8 items-center justify-center rounded-full border-2 p-1 transition hover:text-white"
				>
					<Icon path={mdiTwitter} className="h-16 w-16" />
				</a>
				<a
					href="https://www.linkedin.com/company/crawlink-networks/about/"
					class="border-primary-600 hover:bg-primary-600 flex h-8 w-8 items-center justify-center rounded-full border-2 p-1 transition hover:text-white"
				>
					<Icon path={mdiLinkedin} className="h-16 w-16" />
				</a>
				<a
					href="https://www.youtube.com/@hellocallai"
					class="border-primary-600 hover:bg-primary-600 flex h-8 w-8 items-center justify-center rounded-full border-2 p-1 transition hover:text-white"
				>
					<Icon path={mdiYoutube} className="h-16 w-16" />
				</a>
			</div>
		</div>

		<div class="space-y-4 lg:ps-16">
			<p class="text-base-200 text-base font-semibold">Company</p>
			<ul class="space-y-2">
				<li>
					<a href="/" class="text-base-400 hover:text-primary-500 text-sm transition">Home</a>
				</li>
				<li><a href="/about" class="text-base-400 hover:text-primary-500 text-sm">About Us</a></li>
				<li>
					<a href="/contact" class="text-base-400 hover:text-primary-500 text-sm">Contact Us</a>
				</li>
				<li>
					<a href="/product" class="text-base-400 hover:text-primary-500 text-sm">Products</a>
				</li>

				<li>
					<a href="/product#faq" class="text-base-400 hover:text-primary-500 text-sm">FAQs</a>
				</li>
			</ul>
		</div>

		<div class="space-y-4">
			<p class="text-base-200 text-base font-semibold">We'd love to hear from you!</p>
			<p class="text-base-300">You can reach out to us at:</p>
			<div class="space-y-3">
				<a
					href="tel:+91-8050770132"
					class="hover:text-primary-500 flex items-center justify-center gap-2 text-sm transition lg:items-start lg:justify-start"
				>
					<Icon path={mdiPhone} className="h-4 w-4" />

					+91 6370888479
				</a>
				<a
					href="mailto:lampvoltoffice@gmail.com"
					class="hover:text-primary-500 flex items-center justify-center gap-2 text-sm transition lg:items-start lg:justify-start"
				>
					<Icon path={mdiEmailOutline} className="h-4 w-4" />

					lampvoltoffice@gmail.com
				</a>
				<a
				href="/contact"
				class="bg-primary-500 hover:bg-primary-600 inline-block rounded-full px-6 py-2 font-bold text-white transition"
			>
				Contact Us
			</a>
			</div>
		</div>

		<div class="space-y-4">
			<h6 class="text-base-200 text-base font-semibold">News Letter</h6>
			<div>
				<Newsletter />
			</div>
			
		</div>
	</div>
</div>
