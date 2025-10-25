<script>
	const name = "Mr.DCT"
	const channel = "<b>CodeVolution</b>"
	const hack = `<a href = "#" onclick="alert('You have been hacked!')">Win a price!<a/>`
	const headinID = "heading"
	const disabled = true;
	const status = "success";
	const isPromoted = true;
</script>

<main>
	<h1>Hello {name}</h1>
	<h2 class="underlined">Underlined text</h2>
	<h2 class={status}>Status</h2>
	<!-- class:promoted={isPromoted} is a directive that svetlte provide-->
	<h2 class={isPromoted ? "promoted" : ""}>Movie Title</h2> <!--Ternary operator-->
	<div>{@html channel}</div>
	<div>{@html hack}</div>
	<h2 id = {headinID}>This is a heading</h2>
	<button {disabled}>Bind</button>
</main>

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
	.underlined {
		text-decoration: underline;
	}
	.danger {
		color: red;
	}
	.success {
		color: green;
	}
	.promoted {
		font-style: italic;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>