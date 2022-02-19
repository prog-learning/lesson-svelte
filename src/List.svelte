<script>
  import Item from './Item.svelte';
  export let todos;
  export let removeTodo;
</script>

<ul>
  {#each todos as todo, index}
    <!-- <span>{index}</span> -->
    <Item {todo} {removeTodo} />
  {/each}
</ul>

<style>
</style>
