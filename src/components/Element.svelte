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
div{
    display: flex;
    flex-direction: column;
}
.symbol{
    font-size: 14px;
    font-weight: 900;
    justify-self: center;
    margin: 0px;
}
.name{
    font-weight: 300;
    font-size: 0.5vh;
    justify-self: center;
    margin: 0px;
}
.number {
  float: left;
  font-size: 0.5vw;
  /* position: absolute; */
  
}
</style>
<div>
    <p class="number">{element.number}</p>
    <p class="symbol">{element.symbol}</p>
    <p class="name">{element.name}</p>
</div>