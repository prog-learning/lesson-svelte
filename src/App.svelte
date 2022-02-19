<script>
  import Hello from './Hello.svelte';
  import InputText from './InputText.svelte';
  import List from './List.svelte';

  let todos = [
    {
      id: 1,
      text: 'Learn Svelte',
      completed: false,
    },
    {
      id: 2,
      text: 'Learn Svelte',
      completed: false,
    },
    {
      id: 3,
      text: 'Learn Svelte',
      completed: false,
    },
  ];

  const addTodo = (addText) => {
    /* 代入する判定で再レンダリングされる？ */
    todos = [
      ...todos,
      {
        id: new Date(),
        text: addText,
        completed: false,
      },
    ];
  };

  const removeTodo = (id) => {
    todos = todos.filter((todo) => todo.id !== id);
  };
</script>

<main>
  <!-- <Hello message='渡したいメッセージ' /> -->
  <h1>TO DO APP!!</h1>
  <InputText {addTodo} />
  <List bind:todos {removeTodo} />
  <!-- <button on:click={() => addTodo('aaaa')}>adadada</button> -->
</main>

<style>
</style>
