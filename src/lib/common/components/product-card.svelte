<script lang="ts">
	let { children } = $props();
</script>

<div
	class="rounded-md bg-base-800 shadow-sm border border-base-700 hover:border-primary-400 duration-300 "
>
	<div class="w-full p-4">
		{@render children()}
	</div>
</div>
