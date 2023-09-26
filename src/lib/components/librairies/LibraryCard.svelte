<script lang="ts">
	import { Download, Star, Users } from 'phosphor-svelte';
	import Icon from '$lib/components/Icon.svelte';
	import tempLogo from '$lib/assets/berrybase.png';

	export let item: {
		name: string;
		description: string;
		stars: number;
		downloads: number;
		contributors: number;
	};
	function convertAmount(amount: number) {
		if (amount > 999 && amount <= 999999) {
			return (amount / 1000).toFixed(1) + 'K'; // convert to K for number from > 1000 < 1 million
		} else if (amount > 999999) {
			return (amount / 1000000).toFixed(1) + 'M'; // convert to M for number from > 1 million
		} else if (amount < 900) {
			return amount; // if value < 1000, nothing to do
		}
	}
</script>

<div
	class="bg-slate-200 dark:bg-stone-800 rounded-md border dark:border-stone-700 overflow-hidden relative h-fit"
>
	<div
		class="flex justify-end items-center space-x-2 bg-slate-100 dark:bg-stone-900 p-3 border-b border-slate-200 dark:border-stone-700"
	>
		<div class="text-sm flex ml-3 space-x-1">
			<Icon icon={Star} size={16} /><span>
				{convertAmount(item.stars)}
			</span>
		</div>
		<div class="text-sm flex ml-3 space-x-1">
			<Icon icon={Download} size={16} /><span>
				{convertAmount(item.downloads)}
			</span>
		</div>
		<div class="text-sm flex ml-3 space-x-1">
			<Icon icon={Users} size={16} /><span>
				{convertAmount(item.contributors)}
			</span>
		</div>
	</div>
	<div class="p-3 space-y-2">
		<div class="h-16" />
		<h3 class="text-xl font-bold">
			{item.name}
		</h3>
		<p class="text-sm">{item.description}</p>
	</div>
	<img src={tempLogo} alt="" class="absolute w-24 h-24 object-cover top-4 left-4 rounded-md" />
</div>
