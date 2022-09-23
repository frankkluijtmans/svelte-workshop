<script lang="ts">
    import { slideCount, slideIndex } from '../stores';

    const previous = () => {
        if($slideIndex === 0) return;
        slideIndex.update((n) => n - 1);
    }
    const next = () => {
        if($slideIndex === $slideCount) return;
        slideIndex.update((n) => n + 1);
    }
    const onKeyDown = (e: KeyboardEvent) => {
        switch(e.keyCode) {
            case 37:
                previous();
                break;
            case 39:
                next();
                break;
        }
	}
</script>

<nav id="controls">
    <button class="Control" on:click={previous}>Previous</button>
    <span>{$slideIndex} / {$slideCount}</span>
    <button class="Control" on:click={next}>Next</button>
</nav>

<svelte:window on:keydown={onKeyDown}/>

<style lang="scss">
    #controls {
        position: relative;
        z-index: 1;
        display: flex;
        height: 80px;
        padding: 1rem;
        justify-content: center;
        align-items: center;
        gap: 1rem;
        box-sizing: border-box;
        background-color: var(--color-bg-secondary);
        box-shadow: 0 -4px 16px var(--color-bg-dark);
    }
</style>