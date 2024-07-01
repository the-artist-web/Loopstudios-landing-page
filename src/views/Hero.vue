<template>
  <div class="hero">
    <div class="container">
        <h1 class="title">Immersive<br> experiences<br> that deliver</h1>
    </div>
  </div>
</template>

<script>
export default {
    name: "Hero",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .hero {
        background-image: url(../assets/images/mobile/image-hero.jpg);
        width: 100%;
        height: 100vh;
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center center;
    }
    .hero .container {
        position: relative;
        z-index: 2;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        width: 100%;
        height: 100vh;
    }
    .hero .container .title {
        border: 3px solid var(--White);
        font-family: var(--font-family-Josefin-Sans);
        text-transform: uppercase;
        color: var(--White);
        font-size: 2.8rem;
        font-weight: 300;
        padding: 30px;
        width: 100%;
    }
    
    /*----------------------------------*\
      #MEDIA
    \*----------------------------------*/ 

    /**
     * FIT SIZE 992PX
     */
    @media screen and (min-width: 992px) {
        .hero { background-image: url(../assets/images/desktop/image-hero.jpg); }

        .hero::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            z-index: 1;
        }
        .hero .container .title {
            font-size: 5rem;
            font-weight: 200;
            padding: 35px 70px 35px 35px;
            width: max-content;
        }
    }
</style>