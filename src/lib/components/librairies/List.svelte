<script lang="ts">
	import LibraryCard from '$lib/components/librairies/LibraryCard.svelte';

	const data = [
		{
			id: 1,
			name: 'berrybase',
			description:
				'Fully  featured  and  highly  customizable  Svelte Dashboard template with 100+ components.',
			stars: 1200,
			downloads: 120,
			contributors: 4
		},
		{
			id: 2,
			name: 'berrybase',
			description:
				'Fully  featured  and  highly  customizable  Svelte Dashboard template with 100+ components.',
			stars: 1200,
			downloads: 120,
			contributors: 4
		},
		{
			id: 3,
			name: 'berrybase',
			description:
				'Fully  featured  and  highly  customizable  Svelte Dashboard template with 100+ components.',
			stars: 1200,
			downloads: 120,
			contributors: 4
		},
		{
			id: 4,
			name: 'berrybase',
			description:
				'Fully  featured  and  highly  customizable  Svelte Dashboard template with 100+ components.',
			stars: 1200,
			downloads: 120,
			contributors: 4
		},
		{
			id: 5,
			name: 'berrybase',
			description:
				'Fully  featured  and  highly  customizable  Svelte Dashboard template with 100+ components.',
			stars: 1200,
			downloads: 120,
			contributors: 4
		},
		{
			id: 6,
			name: 'berrybase',
			description:
				'Fully  featured  and  highly  customizable  Svelte Dashboard template with 100+ components.',
			stars: 1200,
			downloads: 120,
			contributors: 4
		}
	];

</script>

<div class="grid grid-cols-1 gap-4 md:grid-cols-2 lg:grid-cols-3 h-fit">
	{#each data as item}
		<LibraryCard {item} />
	{/each}
</div>
