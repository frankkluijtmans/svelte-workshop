<script>
    import DemoArea from "../DemoArea.svelte";
    import DataBinding from "./demos/DataBinding.svelte";
    let name = 'Hobo';
</script>
<ul>
    <li>Inputs</li>
    <li>Component Instance</li>
    <li>Component Props</li>
</ul>

<DemoArea>
    <DataBinding/>
</DemoArea>