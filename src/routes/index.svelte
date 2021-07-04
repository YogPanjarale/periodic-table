<h1> Periodic Table</h1>

<script lang='ts'>
import type { PCElement, PElement } from 'src/types';

    import data from '../data';
    const _data:PElement[]=data.elements as any as PElement[]
    let elements:PCElement[] = []
    for (let i = 1; i <= 118; i++) {
        // console.log(_data[i])
        elements.push({className:`elements element-${i}`,..._data[i]})
    }
    console.log(elements[0])
</script>
<style>
    #table {
        display: grid;
        grid-template-columns: repeat(17,auto) 1fr;
        width: 90%;
        margin: 0 auto;
        max-width: 100%;
    }
    /*Helium to the top right*/
    .element-2{
        grid-column-start: -2;
    }
</style>
<div id="table">
    {#each elements as element }
        <div class={element.className}>{element.symbol}</div>
    {/each}
</div>
