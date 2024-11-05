<script>
  let count = 0
  const increment = () => {
    count += 1
  }
  const decrement = () => {
    count -= 1
  }
</script>

<button on:click={increment} >
 sumar
</button>
<h1>{count}</h1>

<button on:click={decrement}>
  restar
</button>




