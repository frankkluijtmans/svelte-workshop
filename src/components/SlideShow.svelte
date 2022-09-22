<script lang="ts">
    import { slideCount } from '../stores';
    import { onMount } from 'svelte';
    export let currentSlide: number = 0;
    let slideshow;

    onMount(() => {
        slideCount.set(slideshow.children.length - 1);
    });
</script>

<div id="slideshow-wrapper">
    <div 
        id="slideshow"
        bind:this={slideshow}
        style="transform: translateX(calc({currentSlide} * -100%));"
    >
        <slot></slot>
    </div>
</div>

<style lang="scss">
    #slideshow-wrapper {
        overflow: hidden;
        width: 100vw;
        background: var(--color-bg-secondary);
        background: radial-gradient(circle, var(--color-bg) 0%, var(--color-bg-secondary) 100%);
    }

    #slideshow {
        transition: transform 0.3s ease-in-out;
        display: flex;
        height: calc(100vh - 80px);
    }
</style>

