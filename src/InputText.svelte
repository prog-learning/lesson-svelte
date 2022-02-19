<script>
  /* 渡される想定の props は export する */
  // export let message = 'あいさつです' // letはStateとなる
  // const name = '佐藤さん' // 定数の定義
  // const newMessage = message + name // exportは外部から参照できる

  // ここで定義したものはこのファイル内で利用可能

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
