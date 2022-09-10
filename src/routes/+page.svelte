<script>
import Counter from "$lib/Counter.svelte";
	let Debug = false
	let makePencil = function(){
		money++
	}
	let money = 0;
	let onplaynowclick = function(){
		rickroll = true
	}
	let rickroll = false
</script>



<section class="flex flex-col">
	
	<h1 class ="text-4xl text-center">
		{#if money >= 141}
		now im over here!
		{:else if money >= 140}
		im over here now!
		{:else if money >= 135}
		watch this...
		{:else if money >= 115}
		pretty funny right?
		{:else if money >= 110}
		hahahahahaha
		{:else if money >= 100}
		a hundy?
		<button on:click={onplaynowclick} class="bg-white p-1 rounded-md border-2 border-black">you can play now</button>
		
		{#if rickroll == true}
		<img src = "https://c.tenor.com/_4YgA77ExHEAAAAd/rick-roll.gif" alt = "never gonna give you up" class="m-auto">
		
		{/if}
		{:else if money >= 50}
		you have just 50?
		{:else if money >= 10}
		a baby could make more
		{:else if money >= 0}
		ur not cash money
		{/if}
	</h1>
	
	
	
	${money}
	{#if money < 140}
		<button on:click={makePencil} class="ethanBtn">
		make money
		</button>
	{:else if money == 140}
	<button on:click={makePencil} class="ethanBtn fixed left-0 bottom-0">
	make money
	</button>
	{/if}

</section>

	{#if Debug == true}
	<section class="fixed right-0 bottom-0">
		<input type = "text" bind:value={money} />
	</section>
	{/if}
<style>

	.ethanBtn{
		@apply bg-green-600 p-1 rounded-md border-2 border-green-900 active:bg-green-700;
	}
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


