<script>
    import DemoArea from "../DemoArea.svelte";
    import LocalState from "./demos/LocalState.svelte";

</script>
<ul>
    <li>Passed props</li>
    <li>Default prop values</li>
    <li>Dynamic props</li>
    <li>Reactive declarations</li>
</ul>

<DemoArea>
    <LocalState name="Frank"/>
</DemoArea>