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
        background-color: red;
        color: white;
    }
</style>