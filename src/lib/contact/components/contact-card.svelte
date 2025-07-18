<script lang="ts">
	import GlowCard from '$lib/common/components/glow-card.svelte';
	import { mdiEmailOutline, mdiMapMarker, mdiPhone } from '$lib/core/services/app-icons-service';
	import { IconCircle } from '@cloudparker/moldex.js';
</script>

<div class="grid w-full grid-cols-1 gap-4 px-4 md:gap-6 md:px-6 lg:grid-cols-3 lg:px-8">
	<GlowCard>
		<div class="flex flex-col gap-4 md:flex-row">
			<div>
				<IconCircle
					iconPath={mdiEmailOutline}
					iconClassName="text-purple-500  group-hover:text-purple-400 transition-colors duration-300"
				/>
			</div>
			<div class="flex-1 text-left">
				<p class="text-base-100 text-lg font-medium md:text-xl">Email</p>
				<a href="mailto:support@hellocall.ai" class="text-base-400 text-sm md:text-lg">
					lampvoltoffice@gmail.com
				</a>
				<!-- <p class="text-sm text-base-400 md:text-lg">support@hellocall.ai</p> -->
			</div>
		</div>
	</GlowCard>
	<GlowCard>
		<div class="flex flex-col gap-4 md:flex-row">
			<div>
				<IconCircle
					iconPath={mdiPhone}
					iconClassName="text-purple-500 group-hover:text-purple-400 transition-colors duration-300"
				/>
			</div>
			<div class="flex-1 text-left">
				<p class="text-base-100 text-lg font-medium md:text-xl">Phone</p>
				<a href="tel:+919986708492" class="text-base-400 text-sm md:text-lg">+91 6370888479</a>
			</div>
		</div>
	</GlowCard>
	<GlowCard>
		<div class="flex flex-col gap-4 md:flex-row">
			<div>
				<IconCircle
					iconPath={mdiMapMarker}
					iconClassName="text-purple-500 group-hover:text-purple-400 transition-colors duration-300"
				/>
			</div>
			<div class="flex-1 text-left">
				<p class="text-base-100 text-lg font-medium md:text-xl">Address</p>
				<p class="text-base-400 text-sm md:text-lg">
					Dihasarichuan, Cuttack, Odisha, India
				</p>
			</div>
		</div>
	</GlowCard>
</div>
