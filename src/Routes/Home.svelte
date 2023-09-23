<script>
    import { onMount, onDestroy } from "svelte";
    import Section from "../Components/Section.svelte";

    let images = [
        "https://media.photographycourse.net/wp-content/uploads/2022/04/08162559/15-Highly-Creative-Product-Photography-Ideas-reflections.jpeg", //reloj
        "https://assets.easyweddings.com/files/2022/07/28112816/Blue-Ginger-Photography-Wedding-Photographer.jpg", //boda
        "https://www.adorama.com/alc/wp-content/uploads/2018/11/landscape-photography-tips-yosemite-valley-feature-1280x720.jpg", //monte
        "https://expertphotography.b-cdn.net/wp-content/uploads/2019/11/Nighttime-Event-Photography-outside-colour.jpg", //noche
        "https://www.jdinstitute.edu.in/media/2021/07/Types-of-Fashion-Photography-Thumbnail.jpg", //rojo
    ];
    let index = 0;
    let index2 = 1;
    let show = false;
    let show2 = true;
    $: image = images[index];
    $: image2 = images[index2];
    let interval;

    function startInterval() {
        interval = setInterval(() => {
            console.log(index === images.length - 1 && index2 === 0);
            if ((index === images.length - 1 && index2 === 0) || (index2 === images.length - 1 && index === 0)) {
                index === images.length - 1 && index2 === 0 ? (index = 1) : null;
                index2 === images.length - 1 && index === 0 ? (index2 = 1) : null;
            } else {
                index > index2 ? (index2 += 2) : (index += 2);
                index = index > images.length - 1 ? 0 : index;
                index2 = index2 > images.length - 1 ? 0 : index2;
            }

            show = !show;
            show2 = !show2;
        }, 2000);
    }

    onMount(() => {
        startInterval();
    });

    onDestroy(() => {
        clearInterval(interval);
    });
</script>

<Section>
    <img src={image} alt="" class={show ? "show" : "hide"} />
    <img src={image2} alt="" class={show2 ? "show" : "hide"} />
</Section>

<style>
    img {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: all 2s ease;
    }
    .show {
        opacity: 1;
    }
    .hide {
        opacity: 0;
    }
</style>
