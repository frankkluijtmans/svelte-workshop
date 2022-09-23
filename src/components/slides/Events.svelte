<script lang="ts">
    import DemoArea from "../DemoArea.svelte";
    import Events from "./demos/Events.svelte";

    let messageFromChild: string = "";
</script>
<ul>
    <li>on:event</li>
    <li>Special element bindings (window, body, head, component, fragment)</li>
    <li>Event forwarding</li>
    <li>Custom events</li>
</ul>

<DemoArea>
    { messageFromChild }
    <Events on:custom-event={(e) => messageFromChild = e.detail.message}/>
</DemoArea>