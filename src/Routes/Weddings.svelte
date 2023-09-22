<script>
    import Gallery from "../Components/Gallery.svelte";

    let images = [
        "https://www.brides.com/thmb/fJSfAbT8DxJs4dW79wcWZEQZgJs=/1500x0/filters:no_upscale():max_bytes(150000):strip_icc()/must-take-wedding-photos-bride-groom-walk-clary-prfeiffer-photography-0723-primary-b4221bcb1a2b43e6b0820a8c3e3bce52.jpg",
        "https://iso.500px.com/wp-content/uploads/2020/07/Her-By-Melli-Shayne-.jpeg",
        "https://www.lookslikefilm.com/wp-content/uploads/2022/01/Shayne-Thomas-www.instagram.comhowishotthis_weddings.jpg",
        "https://www.silverlightphotography.ca/site/wp-content/uploads/2023/02/171011mp_1018V-min.jpg",
        "https://lh3.googleusercontent.com/atCc8PuP6v7UQibTTME4u89ofaSveTgbAmRhTBOT7S8c-DdRad82c4V0MP6bR__-abifbNafZ4Tw8K8GWYHHq99qRe5JMta1PVOHew=w974-h648-c-l80-e30",
        "https://www.rockmywedding.co.uk/1200x1200/2416/6297/9979/best-wedding-photographers-2022-2.jpg?fit=1",
        "https://cdn0.hitched.co.uk/article/2271/3_2/960/png/121722-jose-hero-image.jpeg",
        "https://www.paulsstudio.co.uk/wp-content/uploads/2022/04/essex-wedding-photographer.jpg",
        "https://assets.easyweddings.com/files/2022/07/28112816/Blue-Ginger-Photography-Wedding-Photographer.jpg",
        "https://images.squarespace-cdn.com/content/v1/523eb97ce4b0a27582758f9f/1550974426971-3EOMIOY09CZJ8Z17ORH8/IGOR+Photography+02-25-19.jpg?format=1500w",
    ];
</script>

<Gallery {images} />