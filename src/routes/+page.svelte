<script>
	let makePencil = function(){
		pencils++
	}
	let pencils = 0;
</script>



<section>
	{#if pencils >= 10}
	<h1>a baby could earn more</h1>
	{:else}
	<h1>ur not cash money</h1>
	{/if}

	
	${pencils}
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
