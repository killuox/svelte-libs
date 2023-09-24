<script lang="ts">
	export let icon: any;
	export let size: number = 20;
	export let weight: 'thin' | 'light' | 'regular' | 'bold' | 'fill' | 'duotone' = 'regular';
	export let color: string = 'currentColor';
	export let style: string = '';
</script>

<svelte:component this={icon} {size} {weight} {color} class={style}/>
