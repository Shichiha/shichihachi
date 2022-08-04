<script>
import Github from "$lib/Github.svelte";


import Home from "$lib/Home.svelte";

</script>
<slot>

</slot>
<div class="sidebar">
    <a href="/"> <Home /></a>
    <a href="/more"> more </a>
</div>

<style>
    a {
        color: #fff;
        text-decoration: none;
        font-size: 35px;
    }
</style>

