<template>
    <section class="box-list section">
        <div class="container">
            <div class="box-list-header">
                <h1 class="title">Our creations</h1>

                <BtnPrimary class="btn-primary"/>
            </div>

            <ul class="img-list">
                <li class="img-item">
                    <img src="../assets/images/mobile/image-deep-earth.jpg" alt="image-deep-earth" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-deep-earth.jpg" alt="image-deep-earth" class="img-desktop img-cover">

                    <h1 class="title-content">Deep<br> earth</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-night-arcade.jpg" alt="image-night-arcade" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-night-arcade.jpg" alt="image-night-arcade" class="img-desktop img-cover">

                    <h1 class="title-content">Night<br> arcade</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-soccer-team.jpg" alt="image-soccer-team" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-soccer-team.jpg" alt="image-soccer-team" class="img-desktop img-cover">

                    <h1 class="title-content">Soccer<br> team VR</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-grid.jpg" alt="image-grid" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-grid.jpg" alt="image-grid" class="img-desktop img-cover">

                    <h1 class="title-content">The<br> grid</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-from-above.jpg" alt="image-from-above" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-from-above.jpg" alt="image-from-above" class="img-desktop img-cover">

                    <h1 class="title-content">From up<br> above VR</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-pocket-borealis.jpg" alt="image-pocket-borealis" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-pocket-borealis.jpg" alt="image-pocket-borealis" class="img-desktop img-cover">

                    <h1 class="title-content">Pocket<br> borealis</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-curiosity.jpg" alt="image-curiosity" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-curiosity.jpg" alt="image-curiosity" class="img-desktop img-cover">

                    <h1 class="title-content">The<br> curiosity</h1>
                </li>
                
                <li class="img-item">
                    <img src="../assets/images/mobile/image-fisheye.jpg" alt="image-fisheye" class="img-mobile img-cover">
                    <img src="../assets/images/desktop/image-fisheye.jpg" alt="image-fisheye" class="img-desktop img-cover">

                    <h1 class="title-content">Make it<br> fisheye</h1>
                </li>
            </ul>

            <BtnPrimary class="btn-primary-desktop"/>
        </div>
    </section>
</template>

<script>
import BtnPrimary from '@/components/BtnPrimary.vue'

export default {
    name: "BoxList",
    components: {
        BtnPrimary
    },
    data() {
        return {}
    }
}
</script>

<style scoped>
    .box-list .container .box-list-header {
        display: flex;
        align-items: center;
        justify-content: center;
        padding-bottom: 40px;
    }
    .box-list .container .box-list-header .title {
        font-family: var(--font-family-Josefin-Sans);
        text-transform: uppercase;
        font-weight: 300;
        font-size: 2.5rem;
    }
    .box-list .container .box-list-header .btn-primary { display: none; }

    .box-list .container .img-list {
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        gap: 25px;
    }
    .box-list .container .img-list .img-item { position: relative; }

    .box-list .container .img-list .img-item img { transition: .4s; }

    .box-list .container .img-list .img-item:hover img { 
        opacity: 0.5; 
        transition: .4s;
    }

    .box-list .container .img-list .img-item:hover .title-content { color: var(--Black); }

    .box-list .container .img-list .img-item .img-desktop { display: none; }

    .box-list .container .img-list .img-item::before {
        content: "";
        background: linear-gradient(80deg, #000 30%,  transparent 100%);
        opacity: 0.5;
        height: 100%;
        width: 100%;
        position: absolute;
        left: 0;
        top: 0;
        bottom: 0;
        z-index: 4;
    }
    .box-list .container .img-list .img-item .title-content {
        font-family: var(--font-family-Josefin-Sans);
        text-transform: uppercase;
        position: absolute;
        left: 20px;
        bottom: 20px;
        color: var(--White);
        font-size: 1.6rem;
        font-weight: 300;
        z-index: 5;
    }
    .btn-primary-desktop { margin: 40px auto; }

    /*----------------------------------*\
      #MEDIA
    \*----------------------------------*/ 

    /**
     * FIT SIZE 992PX
     */
    @media screen and (min-width: 992px) {
        .box-list .container .box-list-header {
            justify-content: space-between;
            padding-bottom: 50px;
        }
        .box-list .container .box-list-header .title { font-size: 3rem; }

        .box-list .container .box-list-header .btn-primary { display: block }

        .box-list .container .img-list { grid-template-columns: repeat(4, 1fr); }

        .box-list .container .img-list .img-item .img-desktop { display: block; }

        .box-list .container .img-list .img-item .img-mobile { display: none; }

        .box-list .container .img-list .img-item::before {
            background: linear-gradient(3600deg, #000 30%,  transparent 100%);
            left: 0;
            top: auto;
            bottom: 0;
            right: 0;
        }
        .box-list .container .img-list .img-item .title-content {
            left: 40px;
            bottom: 40px;
            font-size: 2rem;
        }
        .btn-primary-desktop { display: none; }
    }
</style>