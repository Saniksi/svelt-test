<script>
  let count = 0;
  let string;
  let increment = () => {
    count += 1;
  };

  // $: {
  //   console.log(`The count is ${count}`);
  // }

  $: if (count > 5) {
    console.log(`The count is ${count}`);
  }

  $: string = `You have clicked ${count} times.`
</script>

<button on:click={increment}>Clicks {count}</button>
<h3>{string}</h3>

<h5>You clicked {count}</h5>

<style>
  button {
    padding: 20px;
    font-size: 2em;
  }
</style>
