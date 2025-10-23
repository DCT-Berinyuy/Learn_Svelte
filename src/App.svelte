<!--	JavaScript	-->
<script>
	import { shuffle } from "lodash";
	let names = ["Bruce", "Clark", "Diana", "Barry"];
	const shuffleNames = () => {
		names = shuffle(names);
	};
</script>

<!--	HTML	-->
<main>
	{#each names as name (name)}
		<h2>{name}</h2>
		<input placeholder="Last name" />
	{/each}
	<div>
		<button on:click={shuffleNames}>Shuffle!</button>
	</div>
</main>

<!--	CSS		-->
<style>
	main {
		text-align: center;
		font-family: sans-serif;
	}
</style>