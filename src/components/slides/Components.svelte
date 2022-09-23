<script lang="ts">
    import DemoArea from "../DemoArea.svelte";
    import Slots from "./demos/Slots.svelte";

</script>

<ul>
    <li>Single file components (script, template, styles)</li>
    <li>.svelte extension (VSCode language support)</li>
    <li>Easy switching language for script and styles</li>
    <li>Slots / Named slots / Slot Fallbacks</li>
</ul>

<DemoArea>
    <Slots>
        <div slot="two">This is a slut</div>
    </Slots>
</DemoArea>