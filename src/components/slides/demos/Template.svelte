<script lang="ts">
    let users = [
        { name: 'John', age: 20 },
        { name: 'Jane', age: 24 },
        { name: 'Jim', age: 54 },
    ];
    let promise;

    const getNumber = async() => {
        await new Promise(resolve => setTimeout(resolve, 1000));
        return 1;
    };

    const onClick = () => {
        promise = getNumber();
    }
</script>

<div>
    {#await promise}
        <p>Waiting for promise...</p>
    {:then number}
        <p>Promise resolved with {number}</p>
    {:catch error}
        <p>Promise rejected with {error.message}</p>
    {/await}
    <button on:click={onClick}>Request a number</button>
</div>