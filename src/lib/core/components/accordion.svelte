<script lang="ts">
	import { Icon } from '@cloudparker/moldex.js';
	import { mdiChevronDown, mdiChevronUp, mdiMinus, mdiPlus } from '../services/app-icons-service';
  
	type AccordionData = {
	  title: string;
	  content: string;
	};
  
	type PropsType = {
	  items: AccordionData[];
	  className?: string;
	  iconClassName?: string;
	};
  
	let { items, className = '', iconClassName = '' }: PropsType = $props();
	let activeIndex = $state<number | null>(0);
  
	function toggleAccordion(index: number) {
	  activeIndex = activeIndex === index ? null : index;
	}
  </script>
  
  <div id="accordion-collapse" data-accordion="collapse" class={`space-y-4 ${className}`}>
	{#each items as item, index}
	  <div class="accordion-item border-b border-base-600">
		<h2 id="accordion-collapse-heading-{index}">
		  <button
			type="button"
			class="flex w-full items-start justify-between py-4 md:py-5 font-medium text-base-300 hover:text-base-200 rtl:text-right transition-colors duration-300"
			data-accordion-target="#accordion-collapse-body-{index}"
			onclick={() => toggleAccordion(index)}
			aria-expanded={activeIndex === index}
			aria-controls="accordion-collapse-body-{index}"
		  >
			<span>{item.title}</span>
			<Icon

			  path={activeIndex === index ? mdiMinus : mdiPlus}
			  className={`w-5 h-5 transform transition-transform duration-200 ${activeIndex === index ? 'rotate-180' : ''} hidden md:block ${iconClassName}`}
			  viewBox="0 0 20 20"
			/>
		  </button>
		</h2>
		<div
		  id="accordion-collapse-body-{index}"
		  class="overflow-hidden transition-all duration-300 ease-in-out"
		  style={`max-height: ${activeIndex === index ? '500px' : '0'}; opacity: ${activeIndex === index ? '1' : '0'};`}
		  aria-labelledby="accordion-collapse-heading-{index}"
		>
		  <div class="pb-4 text-base-400">
			{@html item.content}
		  </div>
		</div>
	  </div>
	{/each}
  </div>



  <style>
	/* Smooth accordion transition */
	.accordion-item > div {
		transition: max-height 0.5s ease, opacity 0.3s ease;
	}
</style>