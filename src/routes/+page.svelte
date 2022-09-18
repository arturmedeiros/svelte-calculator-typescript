<script lang="ts">

import Calculator from "../components/Calculator.svelte";

let show = true

</script>

<main>
    {#if show}
        <Calculator />
    {:else}
        <h1>False</h1>
    {/if}
</main>

<style>
    :global(body) {
        background-color: black;
    }

    :root {
        --bg-custom-color: #555;
    }

    main {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }
</style>