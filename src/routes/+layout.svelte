<script lang="ts">
	import { ScreenDetector } from '@cloudparker/moldex.js';
	import '../theme.css';
	import '../tailwind.css';
	
	let { children } = $props();
</script>

<ScreenDetector />
{@render children()}
