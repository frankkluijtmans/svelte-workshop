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
    <button on:click={onClick}>Request a number</button>
</div>