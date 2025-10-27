<script>
    import { createEventDispatcher } from "svelte";
    const dispatch = createEventDispatcher();
</script>

<div>
    <h2>This is a popup</h2>
    <button on:click={() => dispatch('close', "Mr.DCT")}>Close Popup</button>
</div>