<!--	JavaScript	-->
<script>
	let count = 0; //Make sure you use let not const bcs we're going to change count
	function handleClick(event, stepSize) {
		console.log(event)
		count += stepSize;
	}
</script>

<!--	HTML	-->
<main>
	<button on:click={() => (count = count + 1)}>Count {count}</button> <!--In svelte, to listen to an event, we use the on:click-->
	<button on:click={(event) => handleClick(event, 5)}>Count {count}</button>
	<button on:click={(event) => handleClick(event, 10)}>Count {count}</button>
</main>

<!--	CSS		-->
<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>