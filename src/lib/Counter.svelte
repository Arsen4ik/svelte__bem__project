<script>
  export let count = 0;
  const increment = () => {
    count += 1;
  };
</script>

<button on:click={increment} on:mouseenter={() => console.log("mrb")}>
  count is {count}
  {#if true}
    <h1>gg</h1>
  {/if}
  {#each [1, 2, 3] as num, ind}
    {num} - {ind}
  {/each}
</button>
