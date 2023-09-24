<script lang="ts">
	import { Moon, Sun } from 'phosphor-svelte';
	import { onMount } from 'svelte';
	import Icon from './Icon.svelte';

	let isDarkMode = false;

	function handleClick() {
		isDarkMode = !isDarkMode;
		if (isDarkMode) {
			document.body.classList.add('dark');
		} else {
			document.body.classList.remove('dark');
		}
	}

	onMount(() => {
		if (window.matchMedia('(prefers-color-scheme: dark)').matches) {
			isDarkMode = true;
			document.body.classList.add('dark');
		}
	});
</script>

<button on:click={handleClick} class="hover:text-svelte-500">
	{#if isDarkMode}
		<Icon icon={Sun} size={20} />
	{:else}
		<Icon icon={Moon} size={20} />
	{/if}
</button>
