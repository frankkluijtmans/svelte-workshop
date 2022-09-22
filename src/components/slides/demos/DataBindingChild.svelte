<script lang="ts">
    export let name: string = 'No Name';
</script>

<span class="NameBadge">
    {name}
</span>

<style lang="scss">
    .NameBadge {
        background-color: var(--color-bg-secondary);
        padding: 0.5rem;
        border-radius: 0.5rem;
        font-size: 1rem;
        font-weight: bold;
    }
</style>