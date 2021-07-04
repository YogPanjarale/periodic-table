<script lang="ts">
import type { PCElement } from "src/types";


    export let element : PCElement
</script>
<style>
    /* div {
  cursor: pointer;
  width: 5vw;
  height: 5vw;

  padding: 2px;
  border: 1px solid #333;
  border-collapse: collapse;
  overflow: hidden;
} */
/* p{
    
} */
</style>
<div>
    {element.number}
    <p>{element.symbol}</p>
</div>