<!--	JavaScript	-->
<!--Components describe a part of the user interface-->
<!--Probs are custom attributes you can register on a component which allows the component content to be dynamic-->

<script>
	import Greet from "./components/Greet.svelte";
	const name = "Berinyuy"
	const channel = "DCT Lab"
	const obj = {
		name: 'Berry',
		heroName: 'Flash'
	}
</script>

<!--	HTML	-->

<main>
	<Greet name="Verla" heroName="Iron man" />
	<Greet name="Ngu" heroName="Spider man"/>
	<Greet name ="DCT" />
	<Greet {name} heroName={channel} />
	<Greet name={obj.name} heroName={obj.heroName} />
	<!--By using the spread operator-->
	<Greet {...obj} />
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