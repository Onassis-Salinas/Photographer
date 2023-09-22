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

<div class={show}>
    <slot />
</div>

<style>
    div {
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
    @media (max-width: 600px) {
        div {
            margin-top: 80px;
        }
    }
</style>
