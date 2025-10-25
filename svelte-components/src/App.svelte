<!--	JavaScript	-->
<!--Components describe a part of the user interface-->
<script>
	import Greet from "./components/Greet.svelte";
</script>

<!--	HTML	-->

<main>
	<Greet />
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