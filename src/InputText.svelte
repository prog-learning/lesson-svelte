<script>
  let inputState = '';
  export let addTodo;

  const submit = () => {
    if (!inputState) return;
    addTodo(inputState);
    inputState = '';
  };
</script>

<div>
  <input type="text" bind:value={inputState} />
  <button on:click={submit}>add</button>
</div>

<style>
</style>
