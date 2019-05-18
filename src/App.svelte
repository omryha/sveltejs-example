<script>
	let count = 0;
	function increment() {
		count++;
	}
	function decrement() {
		count--;
	}
</script>

<style>
	
</style>

<div>Current count: <input bind:value={count} type="number" /></div>
{#if count > 10}
	<p>So much?!</p>
{:else if count < -5}
	<p>How low can you go?</p>
{:else}
	<p>Keep on clicking them buttons</p>
{/if}
<!--on:eventname-->
<button on:click={increment}>Increment</button>
<button on:click={decrement}>Decrement</button>