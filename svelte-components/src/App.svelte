<!--	JavaScript	-->
<!--Context API provides a way, to pass data through the component tree without having to pass props down manually at every level-->

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