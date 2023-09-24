<script lang="ts">
    import ActionsBar from '$lib/components/librairies/ActionsBar.svelte';
    import List from '$lib/components/librairies/List.svelte';
    import Sidebar from '$lib/components/librairies/Sidebar.svelte';

</script>
<div class="bg-slate-100 dark:bg-stone-900 min-h-screen p-10">
    <ActionsBar />
    <div class="grid grid-row-1 grid-cols-[1fr,3fr] gap-10 mt-10">
        <Sidebar />
        <List />
    </div>
</div>