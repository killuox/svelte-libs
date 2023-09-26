<script lang="ts">
	const data = [
		{
			label: 'UI Components',
			count: 42
		},
		{
			label: 'State Management',
			count: 20
		},
		{
			label: 'Routing',
			count: 15
		},
		{
			label: 'Forms',
			count: 10
		},
		{
			label: 'Animation',
			count: 8
		},
		{
			label: 'Data Visualization',
			count: 25
		},
		{
			label: 'Utilities',
			count: 18
		},
		{
			label: 'Testing',
			count: 12
		},
		{
			label: 'Store',
			count: 7
		},
		{
			label: 'Authentication',
			count: 6
		},
		{
			label: 'Internationalization',
			count: 9
		},
		{
			label: 'Form Validation',
			count: 11
		},
		{
			label: 'File Upload',
			count: 14
		},
		{
			label: 'Notifications',
			count: 13
		},
		{
			label: 'Api',
			count: 5
		},
		{
			label: 'Storage',
			count: 8
		},
		{
			label: 'Audio/Video',
			count: 4
		},
		{
			label: 'Extensions',
			count: 7
		},
		{
			label: 'Responsive Design',
			count: 10
		}
	];
</script>

<div class="flex flex-col">
	<h2 class="text-2xl font-bold mb-4">Categories</h2>
	{#each data as item}
		<button
			class="flex items-center justify-between space-y-2 space-x-2 text-stone-700 dark:text-stone-300 hover:text-svelte-500 dark:hover:text-svelte-500 w-full"
		>
			<span class="text-lg">{item.label}</span>
			<span
				class="text-sm text-slate-500 dark:text-stone-500 border py-1 w-8 text-center rounded-md"
				>{item.count}</span
			>
		</button>
	{/each}
</div>
