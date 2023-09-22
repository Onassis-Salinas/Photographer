<script>
    import Gallery from "../Components/Gallery.svelte";

    let images = [
        "https://www.adorama.com/alc/wp-content/uploads/2018/11/landscape-photography-tips-yosemite-valley-feature-1280x720.jpg",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS3X9L2-TnEkID9xMujtM_0iTzBcmcEbTHzHQ&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSCCia0RPrMPP4sc3qWcv57dgK5iJBg6EOkgA&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSUEQWsrRQZeb_yT3-HL5X-hHWIu9mLJxz1lg&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR69jZp2GHRMRDekzK6-0T3xs5b6Rcvnp7NVA&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsQ78nmIXUPvzW3gZRyCv1yc1agXQxcjRCFw&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQIrs_vDFye4wNFBIakfNoiYZMrgRIzIHPaRA&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ87Tvt8QBCxA3ApXP_KjZASFm6TqfvOm6ZeQ&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSR_9dL3n1IjLx9hX5ULedcQcZXT4wjGIdqCA&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTCI7xfG-_2kQfTZlyCAZSpOkwfvRt93EYZ2w&usqp=CAU",
        "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqBm-ZO5w7lwMNDssHEOn0zYoqZvSs9f_2Tg&usqp=CAU",
    ];
</script>

<Gallery {images} />
