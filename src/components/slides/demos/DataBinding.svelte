<script>
    import DataBindingChild from "./DataBindingChild.svelte";

	let teamName = 'Hobo';
    let isChecked = false;
</script>

<div id="databinding-demo-wrapper">
    <div>
        <input bind:value={teamName}> Hello {teamName}!
    </div>
    
    <div>
        <input id="checkbox" type="checkbox" bind:checked={isChecked}>
        <label for="checkbox">Check me</label>
        <button disabled={!isChecked}>Submit</button>
    </div>

    <div>
        <DataBindingChild bind:name={teamName}/>
    </div>
</div>

<style lang="scss">
    #databinding-demo-wrapper {
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }
</style>