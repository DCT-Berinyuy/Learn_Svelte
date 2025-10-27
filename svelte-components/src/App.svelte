<!--	JavaScript	-->
<!--Context API provides a way, to pass data through the component tree without having to pass props down manually at every level-->

<script>
	import { setContext } from "svelte";
	import ComponentC from "./components/ComponentC.svelte";
	const userName = "Mr.DCT"
	setContext('username-context', userName)
	//Note: The two arguments to setContext right now both are string values
	//but they could be any dataType that your app requres it to be.
	//The 1st argument in fact, what is recommended is to not use a string as the key
	//but instead use an Object literal. Garantees no conflicts
</script>

<!--	HTML	-->

<main>
	<h2>App Component username - {userName}</h2>
	<ComponentC />
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