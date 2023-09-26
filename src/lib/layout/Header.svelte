<script>
	import Logo from '$lib/assets/svelte_logo.png';
	import Darkmode from '$lib/components/Darkmode.svelte';
	import { GithubLogo } from 'phosphor-svelte';
	import Icon from '$lib/components/Icon.svelte';
	import { page } from '$app/stores';

	const links = [
		{
			name: 'Librairies',
			href: '/'
		},

		{
			name: 'About',
			href: '/about'
		}
	];
</script>

<header class="flex items-center justify-between py-4 px-8 bg-slate-200 dark:bg-stone-800">
	<div class="flex items-center">
		<img class="w-8" src={Logo} alt="Svelte Logo" />
		<h1 class="inline-block ml-2 text-2xl font-bold">SvelteLibs</h1>
	</div>
	<nav class="flex items-center">
		{#each links as link}
			<a
				href={link.href}
				class="inline-block mx-2 text-lg cursor-pointer hover:underline hover:text-svelte-500 {$page
					.url.pathname === link.href
					? 'text-svelte-500 underline'
					: ''}"
			>
				{link.name}
			</a>
		{/each}
		<div class="flex ml-4 space-x-2">
			<Darkmode />
			<a href="/" class="hover:text-svelte-500 flex items-center">
				<Icon icon={GithubLogo} size={20} />
			</a>
		</div>
	</nav>
</header>
