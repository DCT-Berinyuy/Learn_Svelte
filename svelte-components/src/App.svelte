<!--	JavaScript	-->
<!--Context API provides a way, to pass data through the component tree without having to pass props down manually at every level-->

<script>
	import Popup from "./components/Popup.svelte";
	let showPopup = false;

	function closPopup(event) {
		showPopup = false;
		console.log(event.detail)
	}
</script>

<!--	HTML	-->

<main>
	<button on:click={() => (showPopup = true)}>Show Popup</button>
	{#if showPopup}
		<Popup on:close={closPopup} />
	{/if}
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