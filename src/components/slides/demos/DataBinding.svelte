<script>
    import DataBindingChild from "./DataBindingChild.svelte";

	let teamName = 'Hobo';
    let isChecked = false;
</script>

<div id="databinding-demo-wrapper">
    <div>
        <input value={teamName}> Hello {teamName}!
    </div>
    
    <div>
        <input id="checkbox" type="checkbox">
        <label for="checkbox">Check me</label>
        <button>Submit</button>
    </div>

    <div>
        <DataBindingChild/>
    </div>
</div>

<style lang="scss">
    #databinding-demo-wrapper {
        display: flex;
        flex-direction: column;
        gap: 2rem;
    }
</style>