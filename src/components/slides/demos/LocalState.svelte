<script lang="ts">
    let count = 0;
</script>

<div>
    <p>Passed prop:</p>
    <p>Dynamic prop: 0 <button on:click={() => {}}>+</button></p>
    <p>Reactive declaration: 2 + 0 = ?</p>
</div>

<style lang="scss">
    button {
        margin-left: 1rem;
    }
</style>