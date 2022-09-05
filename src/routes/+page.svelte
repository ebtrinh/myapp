<script>
	let makePencil = function(){
		money++
	}
	let money = 0;
</script>



<section>
	<h1>
		{#if money >= 100}
		a hundy?
		<a href="/game" >Congrats,  now you can play the game </a>
		{:else if money >= 50}
		you have just 50?
		{:else if money >= 10}
		a baby could make more
		{:else if money >= 0}
		ur not cash money
		{/if}
	</h1>
	

	
	${money}
	<button on:click={makePencil}>
	make money
	</button>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 1;
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
