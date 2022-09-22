<script lang="ts">
    import Slide from './components/Slide.svelte'
    import Controls from './components/Controls.svelte';
    import SlideShow from './components/SlideShow.svelte';
    import { slideIndex } from './stores';
    import Assignment from './components/slides/Assignment.svelte';
    import Routing from './components/slides/Routing.svelte';
    import Animations from './components/slides/Animations.svelte';
    import GlobalState from './components/slides/GlobalState.svelte';
    import Events from './components/slides/Events.svelte';
    import DataBinding from './components/slides/DataBinding.svelte';
    import TemplateSyntax from './components/slides/TemplateSyntax.svelte';
    import LocalState from './components/slides/LocalState.svelte';
    import Components from './components/slides/Components.svelte';
    import Introduction from './components/slides/Introduction.svelte';
    import GettingStarted from './components/slides/GettingStarted.svelte';
</script>

<main>
    <Controls/>
    <SlideShow
        currentSlide={$slideIndex}
    >
        <Slide title="Introduction to Svelte">
            <Introduction/>
        </Slide>
        <Slide title="Component files">
            <Components/>
        </Slide>
        <Slide title="Local state">
            <LocalState/>
        </Slide>
        <Slide title="Template syntax">
            <TemplateSyntax/>
        </Slide>
        <Slide title="Data binding">
            <DataBinding/>
        </Slide>
        <Slide title="Event handling / Custom events">
            <Events/>
        </Slide>
        <Slide title="Global State">
            <GlobalState/>
        </Slide>
        <Slide title="Animations">
            <Animations/>
        </Slide>
        <Slide title="Routing">
            <Routing/>
        </Slide>
        <Slide title="Assignment Time">
            <Assignment/>
        </Slide>
        <Slide title="Getting Started">
            <GettingStarted/>
        </Slide>
    </SlideShow>
</main>

<style lang="scss">
    main {
        display: flex;
        flex-direction: column;
        width: 100vw;
        height: 100vh;
    }
</style>