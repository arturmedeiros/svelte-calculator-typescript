<script lang="ts">
    export let value: string

    $: fontSize = value.length > 20 ? 'small' : `s-${value.length}`
</script>

<div class={`display ${fontSize}`}>
    <span>{value}</span>
</div>

<style>
    .display {
        display: flex;
        flex: 1;
        justify-content: flex-end;
        align-items: center;
        padding: 0px 5px;
        font-size: 1.7rem;
        background-color: aliceblue;
        overflow: hidden;
        margin: 2px 1px;
        border-top-right-radius: 5px;
        border-top-left-radius: 5px;
    }

    .s-10 { font-size: 1.5rem; }
    .s-11 { font-size: 1.35rem; }
    .s-12 { font-size: 1.25rem; }
    .s-13 { font-size: 1.15rem; }
    .s-14 { font-size: 1.07rem; }
    .s-15 { font-size: 1.0rem; }
    .s-16 { font-size: 0.93rem; }
    .s-17 { font-size: 0.87rem; }
    .s-18 { font-size: 0.83rem; }
    .s-19 { font-size: 0.78rem; }
    .s-20 { font-size: 0.74rem; }

    .small { font-size: 0.6rem; }
</style>