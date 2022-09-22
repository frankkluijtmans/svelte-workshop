<script lang="ts">
    export let title: string = 'Slide Title';
</script>

<div class="Slide">
    <h1>{title}</h1>
    <slot></slot>
</div>

<style lang="scss">
    .Slide {
        padding: 3rem;
        height: calc(100vh - 80px);
        box-sizing: border-box;
        flex: 0 0 100vw;
    }
</style>

