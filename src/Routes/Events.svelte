<script>
    import Gallery from "../Components/Gallery.svelte";

    let images = [
        "https://expertphotography.b-cdn.net/wp-content/uploads/2019/11/Nighttime-Event-Photography-outside-colour.jpg",
        "https://s.studiobinder.com/wp-content/uploads/2021/04/Event-photography-examples.jpg?resolution=2560,1",
        "https://dvyvvujm9h0uq.cloudfront.net/com/articles/1580724544-event-5.jpg",
        "https://pbblogassets.s3.amazonaws.com/uploads/2019/03/06130402/shooting-event.jpg",
        "https://photonify.com/wp-content/uploads/2019/01/event-photography-1000x750.jpg",
        "https://shotkit.com/wp-content/uploads/2020/09/event-photography-8.jpg",
        "https://img.youtube.com/vi/eIROwtzhE9k/hqdefault.jpg",
        "https://www.colesclassroom.com/wp-content/uploads/2019/02/pexels-photo-1105666.jpeg",
    ];
</script>

<Gallery {images} />
