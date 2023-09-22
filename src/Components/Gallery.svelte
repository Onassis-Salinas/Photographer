<script>
    import { onMount } from "svelte";
    import Image from "./Image.svelte";

    export let images = [];

    let show = "";
    onMount(() => {
        setTimeout(() => {
            show = "show";
            console.log(show);
        });
    });
</script>

<div class={"container " + show}>
    <div id="gallery">
        {#each images as image}
            <Image src={image} />
        {/each}
    </div>
</div>

<style>
    .container {
        width: 100%;
        height: 100%;
        overflow-y: auto;
        opacity: 0;
        transition: all 1s ease;
    }
    #gallery {
        margin: 15px;
        columns: 3;
        column-width: 230px;
        column-gap: 15px;
    }
    .show {
        opacity: 1;
    }

    .container::-webkit-scrollbar {
        width: 12px;
    }
    .container::-webkit-scrollbar-thumb {
        background-color: var(--primary);
        border-radius: 2px;
    }
    .container::-webkit-scrollbar-track {
        background-color: var(--bg);
    }
    @media (max-width: 600px) {
        .container {
            margin-top: 80px;
            height: calc(100% - 80px);
        }
    }
</style>
