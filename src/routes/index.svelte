<script lang="ts">
	import Element from '../components/element.svelte';
	import type { PCElement, PElement } from 'src/types';

	import data from '../data';
	const _data: PElement[] = (data.elements as any) as PElement[];
	
    function getElements(start:number,end:number):PCElement[] {
        let elements: PCElement[] = [];
        for (let i = start; i <= end; i++) {
		// console.log(_data[i])
		elements.push({ className: `element element-${i}`, ..._data[i] });

        
	}
    // console.log(elements);
    return elements
    }
</script>

<h1>Periodic Table</h1>
<div id="table">
	{#each getElements(1,4) as element}
		<div class={element.className}><Element {element} /></div>
	{/each}
	{#each getElements(5,57) as element}
		<div class={element.className}><Element {element} /></div>
	{/each}
	{#each getElements(72,89) as element}
		<div class={element.className}><Element {element} /></div>
	{/each}
	{#each getElements(104 ,119) as element}
		<div class={element.className}><Element {element} /></div>
	{/each}
	{#each getElements(58 ,71) as element}
		<div class={element.className}><Element {element} /></div>
	{/each}
	{#each getElements(90 ,103) as element}
		<div class={element.className}><Element {element} /></div>
	{/each}
</div>

<style >
	#table {
		display: grid;
		grid-template-columns: repeat(17, auto) 1fr;
		width: 90%;
		margin: 0 auto;
		max-width: 100%;
	}
	/*Helium to the top right*/
	.element-2 {
		grid-column-start: -2;
	}
	/*Boron & Aluminium to the right*/
	.element-5,
	.element-13 {
		grid-column-start: 13;
	}
	/*Lanthanide & Actinides  spilt*/
	.element-58,
	.element-90 {
		grid-column-start: 3;
	}

	/* Disable the top space for the first lathenide which sits inside the table  */
	.element-57 {
		margin: 0;
	}

	.element-119 {
		grid-column-start: -2;
	}
	.element {
		cursor: pointer;
		width: 4vw;
		height: 4vw;

		padding: 2px;
		/* border: 1px solid #333; */
		border-collapse: collapse;
		overflow: hidden;
	}
</style>
