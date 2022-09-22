<script lang="ts">
    import Prism from 'svelte-prism'

    export let source: string;
</script>

<div class="CodeSnippet">
    <Prism 
        {source}
        language="javascript"
    />
</div>