<script>
	import Header from '$lib/layout/Header.svelte';
	import '../app.css';
</script>

<main class="bg-slate-100 dark:bg-stone-900 h-full">
	<Header />
	<slot />
</main>
