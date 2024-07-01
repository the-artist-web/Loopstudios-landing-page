<template>
    <section class="about section">
        <div class="container">
            <img src="../assets/images/mobile/image-interactive.jpg" alt="image-interactive" class="img-mobile img-cover">
            <img src="../assets/images/desktop/image-interactive.jpg" alt="image-interactive" class="img-desktop">

            <div class="about-body">
                <h1 class="title">The leader in<br> interactive VR</h1>
                <p class="text">
                    Founded in 2011, Loopstudios has been producing world-class virtual reality 
                    projects for some of the best companies around the globe. Our award-winning 
                    creations have transformed businesses through digital experiences that bind 
                    to their brand.
                </p>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: "About",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .about { padding-top: 80px; }

    .about .container { position: relative; }

    .about .container .img-desktop { display: none; }

    .about .container .about-body {
        padding-top: 35px;
        text-align: center;
        display: grid;
        gap: 17.5px;
        width: 320px;
        margin: 0 auto;
    }
    .about .container .about-body .title {
        font-family: var(--font-family-Josefin-Sans);
        text-transform: uppercase;
        font-size: 2.3rem;
        font-weight: 300;
    }
    .about .container .about-body .text {
        color: var(--Dark-Gray);
        font-size: 1.1rem;
        line-height: 2;
        font-weight: 400;
    } 

    /*----------------------------------*\
      #MEDIA
    \*----------------------------------*/ 

    /**
     * FIT SIZE 992PX
     */
    @media screen and (min-width: 992px) {
        .about { padding-top: 125px; }

        .about .container .img-desktop { 
            display: block; 
            width: 800px;
        }

        .about .container .img-mobile { display: none; }

        .about .container .about-body {
            background-color: var(--White);
            position: absolute;
            bottom: 0;
            right: 0;
            padding: 100px 0 0 100px;
            text-align: left;
            display: grid;
            gap: 17.5px;
            width: 800px;
            margin: 0 0;
        }
        .about .container .about-body .title { font-size: 4rem; }

        .about .container .about-body .text { max-width: 600px; } 
    }
</style>