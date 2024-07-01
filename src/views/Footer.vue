<template>
    <footer class="footer">
        <div class="container">
            <div class="footer-item">
                <a href="#" class="logo">
                    <img src="../assets/images/logo.svg" alt="logo">
                </a>

                <ul class="navbar-list">
                    <li class="navbar-item">
                        <a href="#" class="nvabar-likn">About</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nvabar-likn">Careers</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nvabar-likn">Events</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nvabar-likn">Products</a>
                    </li>
                    <li class="navbar-item">
                        <a href="#" class="nvabar-likn">Support</a>
                    </li>
                </ul>
            </div>

            <div class="footer-item">
                <div class="social-list">
                    <a href="#" class="social-link">
                        <i class="fa-brands fa-square-facebook"></i>
                    </a>
                    <a href="#" class="social-link">
                        <i class="fa-brands fa-twitter"></i>
                    </a>
                    <a href="#" class="social-link">
                        <i class="fa-brands fa-pinterest"></i>
                    </a>
                    <a href="#" class="social-link">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                </div>
                <p class="copyright">&copy; 2021 Loopstudios. All rights reserved.</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: "Footer",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .footer { 
        background-color: var(--Black); 
        color: var(--White);
        padding: 60px 0;
    }
    .footer .container {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 50px;
    }
    .footer .container .footer-item {
        display: flex;
        flex-direction: column;
        justify-content: center;  
        text-align: center;
    }
    .footer .container .footer-item .logo { margin: 0 auto 40px; }

    .footer .container .footer-item .navbar-list {
        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 20px;
    }
    .footer .container .footer-item .navbar-list .navbar-item .nvabar-likn {
        font-family: var(--font-family-Josefin-Sans);
        text-transform: capitalize;
        color: var(--White);
        padding-bottom: 10px;
        font-size: 1.2rem;
        font-weight: 500;
        position: relative;
        width: max-content;
        margin: 0 auto;
    } 
    .footer .container .footer-item .navbar-list .navbar-item .nvabar-likn::before {
        content: "";
        background-color: var(--White);
        height: 3px;
        width: 40px;
        position: absolute;
        bottom: 0;
        left: 0;
        transform: translateX(-50%);
        visibility: hidden;
        opacity: 0;
    }
    .footer .container .footer-item .navbar-list .navbar-item .nvabar-likn:hover::before {
        left: 50%;
        visibility: visible;
        opacity: 1;
        transition: .4s;
    }
    .footer .container .footer-item .social-list {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 10px;
        gap: 20px;
    }
    .footer .container .footer-item .social-list .social-link {
        font-family: var(--font-family-Josefin-Sans);
        text-transform: capitalize;
        color: var(--White);
        padding-bottom: 5px;
        font-size: 1.8rem;
        font-weight: 500;
        position: relative;
        width: max-content;
    }
    .footer .container .footer-item .social-list .social-link::before {
        content: "";
        background-color: var(--White);
        height: 3px;
        width: 30px;
        position: absolute;
        bottom: 0;
        left: 0;
        transform: translateX(-50%);
        visibility: hidden;
        opacity: 0;
    }
    .footer .container .footer-item .social-list .social-link:hover::before {
        left: 50%;
        visibility: visible;
        opacity: 1;
        transition: .4s;
    }
    .copyright {
        font-size: 1.1rem;
        font-weight: 400;
        color: var(--Very-Dark-Gray);
    }

    /*----------------------------------*\
      #MEDIA
    \*----------------------------------*/ 

    /**
     * FIT SIZE 992PX
     */
    @media screen and (min-width: 992px) {
        .footer .container {
            flex-direction: row;
            justify-content: space-between;
        }
        .footer .container .footer-item {
            justify-content: start;  
            text-align: left
        }
        .footer .container .footer-item .navbar-list {
            flex-direction: row;
            justify-content: center;
            gap: 30px;
        }
        .footer .container .footer-item .logo { margin: 0 0 35px; }

        .footer .container .footer-item .social-list {
            justify-content: end;
            margin-bottom: 20px; 
        }
    }
</style>