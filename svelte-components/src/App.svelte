<!--	JavaScript	-->

<!--
A component's lifecycle refers to the phasese a component
goes through in a Svelte application.
Lifecycle hooks are functions that allows us run code at key moments
during that lifecycle. There are a total of 5 lifecycle
hooks that we can use in a component
1. The onMount hook: The unMount function schedules the passed
in call back to run as soon as the component been mounted to th DOM
2. The onDestroy hook: This schedule a call back 
-->

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