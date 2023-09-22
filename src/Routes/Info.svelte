<script>
    import Section from "../Components/Section.svelte";
</script>

<Section>
    <div class="container">
        <h2>About Me</h2>
        <div id="about">
            <img
                src="data:image/jpeg;base64,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"
                alt=""
            />
            <p>I am a photographer who loves to capture the beauty of the world through my lens. I specialize in landscape, wildlife, and travel photography, and I have been working as a professional photographer for over 10 years. I enjoy exploring new places, meeting new people, and learning about different cultures.</p>
        </div>
    </div>

    <div class="container">
        <h2>Contact</h2>
        <div id="contact">
            <p>+52 664 2956883</p>
            <p>onassis.dev@gmail.com</p>
            <div id="socials">
                <a href="https://facebook.com"><img src="/facebook.svg" alt="" /></a>
                <a href="https://instagram.com"><img src="/instagram.svg" alt="" /></a>
                <a href="https://whatsapp.com"><img src="/whatsapp.svg" alt="" /></a>
            </div>
        </div>
    </div>
</Section>

<style>
    h2 {
        margin: 5px 0 20px 0;
        font-size: 50px;
        text-align: center;
    }
    .container {
        width: min(1000px, 95%);
    }
    #about {
        display: flex;
        justify-content: center;
    }
    #about p {
        font-size: 20px;
        margin: 20px;
        width: 50%;
    }
    #about img {
        margin: 20px;
        width: 250px;
        height: 250px;
        object-fit: cover;
    }

    #socials {
        width: 100%;
        display: flex;
        justify-content: center;
    }
    #socials img {
        width: 60px;
        aspect-ratio: 1;
        margin: 10px;
    }
    #contact p {
        font-size: 25px;
        margin: 0;
        text-align: center;
    }
    @media (max-width: 1000px) {
        #about {
            flex-wrap: wrap;
        }
        #about p {
            width: auto;
        }
        @media (max-width: 450px) {
            #about p {
                font-size: 17px;
            }
        }
    }
</style>
