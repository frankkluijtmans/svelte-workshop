<script>
    import DemoArea from "../DemoArea.svelte";
    import GlobalState from "./demos/GlobalState.svelte";

</script>
<ul>
    <li>Writable state</li>
    <li>Subscriptions</li>
    <li>Read only state</li>
    <li>Derived state</li>
</ul>

<DemoArea>
    <GlobalState/>
</DemoArea>