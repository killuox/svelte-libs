<script>
	import Header from '$lib/layout/Header.svelte';
	import '../app.css';
</script>

<div class="bg-slate-100 dark:bg-stone-900">
	<Header />
	<slot />
</div>
