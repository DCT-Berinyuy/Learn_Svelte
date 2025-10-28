<!--	JavaScript	-->
<!--Slots allow you to re-use a component.
They allow the parent component to control the content inside the child component.
in otherwords, Slots allow a parent component to embed any content in a
child component including HTML elements-->

<script>
	import Card from "./components/Card.svelte";
</script>

<!--	HTML	-->

<main>
	<Card>Card Content</Card>
	<Card><h2>Card Content</h2></Card>
	<Card><img src="https://picsum.photos/200" alt=""></Card>
	<Card />
	<Card>
		<div slot="header">
			<h3>Header</h3>
		</div>
		<div slot="content">
			<img src="https://picsum.photos/200" alt="">
		</div>
		<!--To remove hr, comment footer out-->
		<div slot="footer">
			<button>View Details</button>
		</div>
	</Card>

	<!--<Card content='Card content 1'/>
	<Card content='Card content 2'/> -->

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