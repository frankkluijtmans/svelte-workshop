<div class="DemoArea">
    <slot></slot>
    <span class="Badge">Demo Area</span>
</div>

<style lang="scss">
    .DemoArea {
        position: relative;
        padding: 2rem;
        border-radius: 1rem;
        border: 4px solid var(--color-alt);
        max-width: 700px;
        font-size: 18px;

        .Badge {
            position: absolute;
            bottom: 1rem;
            right: 1rem;
            padding: 0 0.5rem;
            background-color: var(--color-alt-secondary);
            border-radius: 0.5rem;
            color: var(--color-bg-dark);
            font-size: 12px;
            text-transform: uppercase;
            font-weight: 500;
        }
    }
</style>