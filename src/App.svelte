<!--	JavaScript	-->
<!--
In Svelte, a reactive declaration is a special syntax that allows you to declare variables whose values automatically recompute whenever their dependencies change. This is a core part of Svelte's reactivity system, enabling efficient updates to the UI without the need for a virtual DOM.
The syntax for a reactive declaration uses a labeled statement with a dollar sign and a colon ($:), followed by the variable declaration and its assignment.-->
<script>
  import { identity } from "svelte/internal";

	let firsName = "Verla"
	let lastName = "Berinyuy"
	$: fullName = `${firsName} ${lastName}`
	$: {
		const greet = `Full name is ${fullName}`
		console.log(greet)
	}
	let items = [
		{
			id: 1,
			title: 'TV',
			price: 100
		},
		{
			id: 2,
			title: 'Phone',
			price: 200
		},
		{
			id: 3,
			title: 'Laptop',
			price: 300
		}
	]
	$: total = items.reduce((total, curr) => (total = total + curr.price), 0)
	let volume = 0;
	$: if (volume < 0) {
		alert(`Can't go lower`)
		volume = 0;
	} else if (volume > 20) {
		alert(`Can't go higher`)
		volume = 20;
	}
</script>

<!--	HTML	-->
<main>
	<h2>Current volume {volume}</h2>
	<button on:click={() => (volume += 2)}>Increase volume</button>
	<button on:click={() => (volume -= 2)}>Decrease volume</button>
	<button on:click={() => {
		firsName = 'Rejoice'
		lastName = 'Ngu'
	}}>Change name</button>
	<h2>{firsName} {lastName}</h2>
	<h1>{fullName}</h1>
	<button on:click={() => (items = [...items, {id: 4, title: 'keyboard', price: 50}])}
	>Add item</button>
	<h2>
		Total - {total}
	</h2>
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