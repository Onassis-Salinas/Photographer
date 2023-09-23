<script>
    import { Router, Link } from "svelte-routing";
</script>

<div id="sidebar">
    <h4>Photographer</h4>
    <Router>
        <Link to="/" on:click={()=>console.log("Hola")}>Home</Link>
        <Link to="/info">Info</Link>
        <p></p>
        <Link to="/products">Products</Link>
        <Link to="/weddings">Weddings</Link>
        <Link to="/landscape">Landscape</Link>
        <Link to="/events">Events</Link>
        <Link to="/fashion">Fashion</Link>
    </Router>
</div>

<style>
    h4 {
        font-size: 40px;
        margin: 10px 0 60px 0;
    }

    #sidebar {
        display: flex;
        justify-content: flex-start;
        flex-direction: column;
        background-color: var(--primary);
        width: 300px;
        padding: 10px;
        z-index: 999;
    }
    p{
        margin: 5px;
    }
</style>
