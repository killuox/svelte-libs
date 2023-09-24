<script lang="ts">
	import * as Tabs from '$lib/components/ui/tabs';
	import { Download, Clock, Star, Plus, SortAscending } from 'phosphor-svelte';
	import Icon from '$lib/components/Icon.svelte';
	import { Input } from '$lib/components/ui/input';
</script>

<div class="flex items-center justify-between space-x-2">
    <Input class="bg-slate-200 dark:bg-stone-800 max-w-xs" type="text" placeholder="Search..." />
	<div class="flex items-center space-x-2">
		<Tabs.Root value="downloads" class="w-[400px]">
			<Tabs.List class="bg-slate-200 dark:bg-stone-800">
				<Tabs.Trigger value="downloads">
					<div class="flex items-center space-x-2">
						<Icon icon={Download} size={16} />
						<span class="">Downloads</span>
					</div>
				</Tabs.Trigger>
				<Tabs.Trigger value="stars">
					<div class="flex items-center space-x-2">
						<Icon icon={Star} size={16} />
						<span class="">Stars</span>
					</div>
				</Tabs.Trigger>
				<Tabs.Trigger value="new">
					<div class="flex items-center space-x-2">
						<Icon icon={Plus} size={16} />
						<span class="">New</span>
					</div>
				</Tabs.Trigger>
				<Tabs.Trigger value="updated">
					<div class="flex items-center space-x-2">
						<Icon icon={Clock} size={16} />
						<span class="">Updated</span>
					</div>
				</Tabs.Trigger>
			</Tabs.List>
		</Tabs.Root>
		<button class="p-2.5 rounded-md bg-slate-200 dark:bg-stone-800">
			<Icon icon={SortAscending} size={20} />
		</button>
	</div>
</div>
