<script lang="ts">
    export let name: string;
    let count: number = 0;
    $: sum = 2 + count;
    const onIncrement = () => {
        if(count < 10) count++;
    }
</script>

<div>
    <p>Passed prop: {name}</p>
    <p>Dynamic prop: {count} <button on:click={onIncrement}>+</button></p>
    <p>Reactive declaration: 2 + {count} = {sum}</p>
</div>

<style lang="scss">
    button {
        margin-left: 1rem;
    }
</style>