<script lang="ts">
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();
</script>

<div>
    <button on:click={() => dispatch('custom-event', { message: 'Hi Hobo!' })}>Click me!</button>
</div>