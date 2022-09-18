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
        font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
        background-color: black;
    }

    :global(html) {
        font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
        padding: 0;
        margin: 0;
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

    /* Responsive */
    @media only screen and (max-width: 600px) {
        :global(body) {
            background-color: black;
            padding: 0;
            margin: 0;
        }
    }
</style>