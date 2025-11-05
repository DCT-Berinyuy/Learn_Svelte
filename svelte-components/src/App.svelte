<!--	JavaScript	-->

<script>
import ChildStyle from "./components/ChildStyle.svelte";
</script>

<!--	HTML	-->

<main>
	<h3>App component global style</h3>
	<h4>Appp component text</h4>
	<ChildStyle />

</main>

<!--	CSS		-->

<style>
	:global(h3) {
		color: blue;
	}
	h4 {
		color: olive;
	}
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