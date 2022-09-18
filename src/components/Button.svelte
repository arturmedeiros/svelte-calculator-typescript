<script lang="ts">
    export let text: string
    export let triple: boolean = false
    export let double: boolean = false
    export let operation: boolean = false
    export let feature: boolean = false
    export let onClick: (valor: string) => void = () => {}
</script>

<button class="btn"
        on:click={() => onClick(text)}
        class:triple class:double class:operation class:feature>
    {text}
</button>

<style>
    .btn {
        margin: 0;
        border: 1px solid var(--bg-custom-color);
        flex-basis: 25%;
        color: black;
        background-color: #b0b0b0;
    }

    .triple {
        flex-basis: 75%;
    }

    .double {
        flex-basis: 50%;
    }

    .operation {
        background-color: orange;
        color: white;
    }

    .feature {
        background-color: white;
        color: #000000;
    }

    /* Responsive */

    @media only screen and (max-width: 600px) {
        .btn {
            font-family: Inter, Avenir, Helvetica, Arial, sans-serif;
            font-size: 30px;
            font-weight: 500;
            border: 1px solid #000;
            margin: 5px;
            height: 11vh;
            border-radius: 15px;
            background-color: #b0b0b0;
        }


        .operation {
            background-color: orange;
            color: white;
        }

        .feature {
            background-color: white;
            color: #000000;
        }
    }
</style>