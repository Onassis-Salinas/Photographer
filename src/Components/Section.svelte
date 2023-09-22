<script>
    import { onMount } from "svelte";

    let show = "";
    onMount(() => {
        setTimeout(() => {
            show = "show";
            console.log(show);
        });
    });
</script>

<div class={"container " + show}>
    <slot />
</div>

<style>
    .container {
        width: 100%;
        opacity: 0;
        transition: all 1s ease;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        flex-direction: column;
        position: relative;
        overflow-y: auto;
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
        }
    }
</style>
