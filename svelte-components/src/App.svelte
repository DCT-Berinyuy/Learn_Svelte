<!--	JavaScript	-->
<!--Event forwarding helps you listen to and event in a deeply nested component-->

<script>
	import Outer from "./components/Outer.svelte";
	import Button from "./components/Button.svelte";

	function handleGreet(event) {
		alert(event.detail)
	}
</script>

<!--	HTML	-->

<main>
	<Outer on:greet={handleGreet} />
	<Button on:click={() => alert('Clicked')}>Click</Button>
</main>

<!--	CSS		-->

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>