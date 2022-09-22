<script lang="ts">
    import { writable } from 'svelte/store';
    //import { spring } from 'svelte/motion';
    //import { fade } from 'svelte/transition';

    const offset = writable(0);
    let visible = true;

    const animateCircle = () => { offset.set(-100) };
</script>

<div id="animations-demo-wrapper">
    <div class="Circle" style="transform: translateX(-{$offset}px);"/>
</div>
<button on:click={animateCircle}>Animate</button>

<style lang="scss">
    #animations-demo-wrapper {
        display: flex;
        height: 300px;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        .Circle {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background-color: var(--color-alt);
        }
    }
</style>