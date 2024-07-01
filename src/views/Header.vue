<template>
  <header class="header">
    <div class="container">
        <a href="#" class="logo">
            <img src="../assets/images/logo.svg" alt="logo">
        </a>

        <nav class="navbar" data-navbar>
            <div class="navbar-header">
                <a href="#" class="logo">
                    <img src="../assets/images/logo.svg" alt="logo">
                </a>

                <button @click="hiddenNavbar()">
                    <img src="../assets/images/icon-close.svg" alt="icon-close" class="icon">
                </button>
            </div>

            <ul class="navbar-list">
                <li class="navbar-item">
                    <a href="#" class="navbar-link">About</a>
                </li>
                <li class="navbar-item">
                    <a href="#" class="navbar-link">Careers</a>
                </li>
                <li class="navbar-item">
                    <a href="#" class="navbar-link">Events</a>
                </li>
                <li class="navbar-item">
                    <a href="#" class="navbar-link">Products</a>
                </li>
                <li class="navbar-item">
                    <a href="#" class="navbar-link">Support</a>
                </li>
            </ul>
        </nav>

        <button @click="showNavbar()">
            <img src="../assets/images/icon-hamburger.svg" alt="icon-hamburger" class="icon">
        </button>
    </div>
  </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {}
    },
    methods: {
        showNavbar: function() { document.querySelector("[data-navbar]").classList.add("active"); },
        hiddenNavbar: function() { document.querySelector("[data-navbar]").classList.remove("active"); }
    }
}
</script>

<style scoped>
    .header .container {
        height: 130px;
        width: 100%;
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        display: flex;
        align-items: center;
        justify-content: space-between;
        z-index: 10;
    }
    .header .container .navbar {
        position: fixed;
        top: -1000px;
        right: 0;
        bottom: 0;
        background-color: var(--Black);
        width: 100%;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        padding: 16px;
        z-index: 10;
        transition: .6s;
    }
    .header .container .navbar.active {
        top: 0;
        transition: .6s;
    }
    .header .container .navbar .navbar-header {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding-inline: 16px;
        position: absolute;
        height: 130px;
        width: 100%;
        top: 0;
        left: 0;
        right: 0;
    }
    .header .container .navbar .navbar-list {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
    .header .container .navbar .navbar-list .navbar-item .navbar-link {
        font-family: var(--font-family-Josefin-Sans);
        text-transform: uppercase;
        color: var(--White);
        padding-bottom: 10px;
        font-size: 2.8rem;
        font-weight: 300;
        position: relative;
        width: max-content;
    }
    .header .container .navbar .navbar-list .navbar-item .navbar-link::before {
        content: "";
        background-color: var(--White);
        height: 5px;
        width: 70px;
        position: absolute;
        bottom: 0;
        left: 0;
        transform: translateX(-50%);
        visibility: hidden;
        opacity: 0;
    }
    .header .container .navbar .navbar-list .navbar-item .navbar-link:hover::before {
        left: 50%;
        visibility: visible;
        opacity: 1;
        transition: .4s;
    }
    .icon { 
        width: 28px; 
        transition: .4s;
    }
    .icon:hover { 
        transform: rotate(360deg);
        transition: .4s;
    }

    /*----------------------------------*\
      #MEDIA
    \*----------------------------------*/ 

    /**
     * FIT SIZE 992PX
     */
    @media screen and (min-width: 992px) {
        .header .container { height: 150px; }

        .header .container .navbar {
            position: static;
            background-color: transparent;
            width: 100%;
            height: 0;
            padding: 0;
            display: flex;
            justify-content: end;
        }
        .header .container .navbar .navbar-header { display: none; }

        .header .container .navbar .navbar-list {
            display: flex;
            flex-direction: row;
            gap: 30px;
        }
        .icon {  display: none; }
        
        .header .container .navbar .navbar-list .navbar-item .navbar-link {
            text-transform: capitalize;
            font-size: 1.1rem; 
            font-weight: 400;
        }
        .header .container .navbar .navbar-list .navbar-item .navbar-link::before {
            height: 3px;
            width: 30px;
        }
    }
</style>