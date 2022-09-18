<script lang="ts">
    // Import Model
    import CalculatorModel from "../model/CalculatorModel";

    // Import Components
    import Button from "./Button.svelte";
    import Display from "./Display.svelte";
    import Line from "./Line.svelte";

    // Model Initialized
    let calc = new CalculatorModel()

    // Constants
    const calculate = () => calc = calc.calculate()
    const clear = () => calc = calc.clear()
    const typedNumber = (num: string) => calc = calc.typedNumber(num)
    const typedOperation = (op: string) => calc = calc.typedOperation(op)
    const typedPoint = () => calc = calc.typedPoint()

</script>

<div class="calculator">
    <Display value={calc.value} />
    <Line>
        <Button feature triple text="AC" onClick={clear} />
        <Button operation text="/" onClick={typedOperation} />
    </Line>
    <Line>
        <Button text="7" onClick={typedNumber} />
        <Button text="8" onClick={typedNumber} />
        <Button text="9" onClick={typedNumber} />
        <Button operation text="*" onClick={typedOperation} />
    </Line>
    <Line>
        <Button text="4" onClick={typedNumber} />
        <Button text="5" onClick={typedNumber} />
        <Button text="6" onClick={typedNumber} />
        <Button operation text="+" onClick={typedOperation} />
    </Line>
    <Line>
        <Button text="1" onClick={typedNumber} />
        <Button text="2" onClick={typedNumber} />
        <Button text="3" onClick={typedNumber} />
        <Button operation text="-" onClick={typedOperation} />
    </Line>
    <Line>
        <Button double text="0" onClick={typedNumber} />
        <Button text="," onClick={typedPoint} />
        <Button feature text="=" onClick={calculate} />
    </Line>
</div>

<style>
    .calculator {
        background-color: var(--bg-custom-color);
        height: 220px;
        width: 150px;
        padding: 10px;
        border-radius: 10px;
        display: flex;
        flex-direction: column;
    }
</style>