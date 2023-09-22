<script>
	import Logo from '$lib/assets/svelte_logo.png';
	import Darkmode from '$lib/components/Darkmode.svelte';
</script>

<header class="flex items-center justify-between p-3 px-8">
	<div class="flex items-center">
		<img class="w-8" src={Logo} alt="Svelte Logo" />
		<h1 class="inline-block ml-2 text-2xl font-bold">SvelteLibs</h1>
	</div>
	<nav class="flex items-center">
		<a class="inline-block mx-2 text-lg cursor-pointer hover:underline hover:text-svelte-500"
			>Librairies</a
		>
		<a class="inline-block mx-2 text-lg cursor-pointer hover:underline hover:text-svelte-500"
			>Requests</a
		>
		<a class="inline-block mx-2 text-lg cursor-pointer hover:underline hover:text-svelte-500"
			>About</a
		>
		<Darkmode />
	</nav>
</header>
