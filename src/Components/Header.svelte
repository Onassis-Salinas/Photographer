<script>
    import { Link, Router } from "svelte-routing";

    let show = false;
    function handleClick() {
        show = !show;
    }
</script>

<header>
    <p>Photographer</p>
    <img src="/menu.svg" alt="" on:click={handleClick} />
</header>
<div class={"options " + (show ? "show" : "")}>
    <Router>
        <div on:click={handleClick}><Link to="/">Home</Link></div>
        <div on:click={handleClick}><Link to="/info">Info</Link></div>
        <span />
        <div on:click={handleClick}><Link to="/products">Products</Link></div>
        <div on:click={handleClick}><Link to="/weddings">Weddings</Link></div>
        <div on:click={handleClick}><Link to="/landscape">Landscape</Link></div>
        <div on:click={handleClick}><Link to="/events">Events</Link></div>
        <div on:click={handleClick}><Link to="/fashion">Fashion</Link></div>
    </Router>
</div>

<style>
    header {
        position: fixed;
        width: 100%;
        height: 80px;
        z-index: 999;
        background-color: var(--primary);
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .options {
        position: absolute;
        left: 0;
        right: 0;
        top: -500px;
        z-index: 998;
        background-color: var(--primary);
        height: 250px;
        transition: all 1s ease;
        display: flex;
        flex-direction: column;
        padding: 20px;
    }

    .options span {
        margin: 8px;
    }

    header p {
        font-size: 30px;
        margin: 20px;
    }
    img {
        width: 40px;
        margin: 20px;
    }
    .show {
        top: 80px;
    }
</style>
