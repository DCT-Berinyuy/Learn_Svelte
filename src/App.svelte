<!--	JavaScript	-->
<script>
	const names = ['Mr.DCT', 'Ama', 'NNR'];
	const fullNames = [
		{first: "Verla", last: "Berinyuy"},
		{first: "Ama", last: "Morel"},
		{first: "Nkemalo", last: "Rejoice"},
	];
</script>

<!--	HTML	-->
<main>
	{#each fullNames as name, index}
		<h2>{index + 1} {name.first} {name.last}</h2>
	{/each}

	{#each names as name, index}
		<h2>{index + 1} {name}</h2>
	{/each}
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