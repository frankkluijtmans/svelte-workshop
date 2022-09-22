<script lang="ts">
    import Prism from 'svelte-prism'
    import CodeSnippet from '../CodeSnippet.svelte';
</script>

<ul>
    <li>Built in with SvelteKit</li>
    <li>
        Third party routing libraries (e.g. svelte-routing)
        <CodeSnippet source={`npm install svelte-routing`} />
        <CodeSnippet source={`<!-- App.svelte -->
<script>
    import { Router, Link, Route } from "svelte-routing";
    import Home from "./routes/Home.svelte";
    import About from "./routes/About.svelte";
    import Blog from "./routes/Blog.svelte";

    export let url = "";
</script>

<Router url="{url}">
    <nav>
    <Link to="/">Home</Link>
    <Link to="about">About</Link>
    <Link to="blog">Blog</Link>
    </nav>
    <div>
    <Route path="blog/:id" component="{BlogPost}" />
    <Route path="blog" component="{Blog}" />
    <Route path="about" component="{About}" />
    <Route path="/"><Home /></Route>
    </div>
</Router>`}/>
    </li>
</ul>