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
    console.log('addTodo', addText);
    /* 代入する判定が大事 */
    // todos.push({
    //   id: new Date(),
    //   text: addText,
    //   completed: false,
    // });
    todos[0].text = 'qaaaaa';
    todos = todos;
    // todos = [
    //   ...todos,
    //   {
    //     id: new Date(),
    //     text: addText,
    //     completed: false,
    //   },
    // ];
  };

  const removeTodo = (id) => {
    console.log(todos);

    console.log('removeTodo', id);
    todos = todos.filter((todo) => todo.id !== id);
  };
  console.log('app render');
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
