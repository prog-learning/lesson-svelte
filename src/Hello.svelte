<script>
  /* 渡される想定の props は export する */
	export let message = 'あいさつです' // letはStateとなる
  const name = '佐藤さん' // 定数の定義
  const newMessage = message + name // exportは外部から参照できる

// ここで定義したものはこのファイル内で利用可能
</script>

<main>
	<h1>{newMessage}!</h1>
</main>

<style>

</style>