<script lang="ts">
	import Accordion from "$lib/core/components/accordion.svelte";
	import { faqData } from "./faq";

	
</script>

<div class="w-full px-4 md:px-16 lg:px-32 py-4 md:py-6 lg:py-12">
	<h2 class="text-2xl font-bold text-center mb-8 md:mb-12 text-white">
		You asked, we answered
	</h2>
	<Accordion items={faqData} className="" iconClassName="text-base-300" />
</div>
