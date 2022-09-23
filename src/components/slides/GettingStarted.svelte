<script lang="ts">
    import Prism from 'svelte-prism'
    import CodeSnippet from '../CodeSnippet.svelte';
</script>

<ul>
    <li>
        Set up your project using these commands
        <CodeSnippet source={`npm create vite@latest myapp -- --template svelte-ts
cd myapp
npm install
npm run dev`}/>
    </li>
    <li>
        Use a component library if you want (e.g. https://sveltematerialui.com/)
    </li>
    <li>Optional: install <code>node-sass</code> if you'd like to use scss</li>
</ul>