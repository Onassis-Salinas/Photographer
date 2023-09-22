<script>
    import { onMount } from "svelte";
    import { Router, Route } from "svelte-routing";
    import SideBar from "./Components/SideBar.svelte";
    import Header from "./Components/Header.svelte";
    import Home from "./Routes/Home.svelte";
    import Info from "./Routes/Info.svelte";
    import Products from "./Routes/Products.svelte";
    import Weddings from "./Routes/Weddings.svelte";
    import Landscape from "./Routes/Landscape.svelte";
    import Fashion from "./Routes/Fashion.svelte";
    import Events from "./Routes/Events.svelte";

    // let vars = "--text: #000;--bg: #fff;--primary: #818D8C;--secondary: #d3ecac;--accent: #a52775;";
    let vars = "--text: #fff;--bg: #000;--primary: #222;--secondary: #d3ecac;--accent: #a52775;";
    let width = 0;

    onMount(() => {
        width = window.innerWidth;
    });
    window.addEventListener("resize", () => {
        width = window.innerWidth;
        console.log(width);
    });
</script>

<main style={vars}>
    {#if width > 600}
        <SideBar />
    {:else}
        <Header />
    {/if}

    <Router>
        <Route path="/"><Home /></Route>
        <Route path="/info"><Info /></Route>
        <Route path="/products"><Products /></Route>
        <Route path="/weddings"><Weddings /></Route>
        <Route path="/landscape"><Landscape /></Route>
        <Route path="/events"><Events /></Route>
        <Route path="/fashion"><Fashion /></Route>
    </Router>
</main>

<style>
    main {
        color: var(--text);
        background-color: var(--bg);
        width: 100%;
        height: 100%;
        display: flex;
        font-family: "Oswald", sans-serif;
    }
</style>
