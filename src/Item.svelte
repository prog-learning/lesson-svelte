<script>
  export let todo;
  export let removeTodo;
  console.log('item render');
</script>

<li>
  <input type="checkbox" bind:checked={todo.completed} />
  <span class={`${todo.completed && 'checked'}`}>{todo.text}</span>
  {#if todo.completed}
    <button on:click={removeTodo(todo.id)}>×</button>
  {:else if todo.text.includes('todo')}
    <button disabled>やらなきゃだよ</button>
  {:else}
    <button disabled>消せないよ</button>
  {/if}
</li>

<style>
  li {
    list-style: none;
    display: flex;
    align-items: center;
    padding: 10px;
    border-bottom: 1px solid #ccc;
  }
  input {
    margin-right: 10px;
  }
  .checked {
    text-decoration: line-through;
    color: gray;
  }
</style>
