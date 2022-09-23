<script lang="ts">
    import { elapsed, time, sampleState } from "../../../stores";
</script>

<div>
    <p>Value from state: {$sampleState}</p>
    <p>The current time is: {$time}?</p>
    <p>It has been {$elapsed} seconds since this presentation started.</p>
</div>