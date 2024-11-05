<script>
  import Header from "./lib/Header.svelte";
  import Contador from "./lib/Contador.svelte";
  import DarkMode from "./lib/DarkMode.svelte";
  import Galeria from "./lib/Galeria.svelte";

  let colores = ["cyan", "yellow", "red", "orange", "purple", "brown", "aqua"];
</script>

{#each colores as color, i}
  {#if i % 2}
    <Header {color} titulo={color} tamano={3} />
  {:else}
    <Header {color} titulo={color} tamano={2} />
  {/if}
{/each}

<Contador/>
<DarkMode>cambaircolor</DarkMode>

<style>
  :global(body) {
		background-color: #f2eee2;
		color: #0084f6;
		transition: background-color 0.3s
	}
	:global(body.dark-mode) {
		background-color: #1d3040;
		color: #bfc2c7;
	}
  

  main {
    text-align: center;
    margin: 20px;
  }


  
</style>



<main>
  <h1>Galería de img</h1>
  <Galeria />
</main>


