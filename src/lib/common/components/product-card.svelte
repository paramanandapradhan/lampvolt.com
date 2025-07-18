<script lang="ts">
	let { children } = $props();
</script>

<div
	class="transform rounded-md bg-base-700 shadow-sm transition-transform duration-300 hover:scale-105"
>
	<div class="w-full p-4">
		{@render children()}
	</div>
</div>
