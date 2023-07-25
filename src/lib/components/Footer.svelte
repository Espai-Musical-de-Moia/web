<script>
    import iconMail from "$lib/img/footer/icon_mail.svg";
    import iconTelephone from "$lib/img/footer/icon_telephone.svg";
    import iconInstagram from "$lib/img/footer/icon_intagram.svg";
    import iconFacebook from "$lib/img/footer/icon_facebook.svg";
    import iconYouTube from "$lib/img/footer/icon_youtube.svg";
    import logo from "$lib/img/header/logo.png";
</script>

<footer>
    <div class="logo">
        <img class="footer-logo" src={logo} alt="logoPrincipal" />
    </div>
    <hr />
    <section>
        <div class="reds">
            <a href="https://www.instagram.com/espaimusical.moia/"
                ><img src={iconInstagram} alt="instagram" /></a
            >
            <a href="https://www.facebook.com/EspaiMusicalMoia/"
                ><img src={iconFacebook} alt="facebook" /></a
            >
            <a
                href="https://www.youtube.com/channel/UCYNZvFj4dcFcXlQLyicGAVw?view_as=subscriber"
                ><img src={iconYouTube} alt="youtube" /></a
            >
        </div>

        <div class="contacte">
            <div class="mail">
                <img src={iconMail} alt="correu" />
                <p>espaimusical.moia@gmail.com</p>
            </div>

            <div class="phone">
                <img src={iconTelephone} alt="telefon" />
                <p>+34 627949433 (Dani)<br /><br />+34 655333709 (Queralt)</p>
            </div>
        </div>

        <div class="avis">
            <p>Avís Legal</p>
            <p>Política de Cookies</p>
            <p>Política de Privacitad</p>
        </div>

        <div class="documentacio">
            <p>
                <a
                    href="https://drive.google.com/file/d/1t4vk2pkykzVGLiYUyEee_l28WNiidL8s/view"
                    >Drets d'imatge</a
                >
            </p>
        </div>
    </section>
</footer>

<style>
    footer {
        margin: auto;
        width: 100%;
        box-sizing: border-box;
        background-color: #07090d;
        bottom: 0;
        height: 20%;
    }

    section {
        display: flex;
        justify-content: space-around;
    }

    a:link {
        color: white;
        background-color: transparent;
        text-decoration: none;
    }

    a:visited {
        color: white;
        background-color: transparent;
        text-decoration: none;
    }

    a:hover {
        color: white;
        background-color: transparent;
        text-decoration: none;
    }

    a:active {
        color: white;
        background-color: transparent;
        text-decoration: none;
    }

    .logo {
        width: 100%;
        display: flex;
        justify-content: center;
    }

    .footer-logo {
        max-width: 5%;
        max-height: 9%;
    }

    img {
        max-width: 18%;
    }
    p {
        font-size: 12px;
        color: #ffffff;
    }

    hr {
        height: 1px;
        background-color: rgba(0, 0, 0, 0.3);
        box-shadow: 0px 1px 3px rgba(0, 0, 0, 0.4);
        opacity: 0.3;
    }

    .contacte {
        display: flex;
        flex-direction: column;
    }

    .mail {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;
    }

    .phone {
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: 10px;
    }

    .avis {
        text-align: center;
    }

    .documentacio {
        text-align: center;
    }

    @media screen and (max-width: 575px) {
        p {
            font-size: xx-small;
        }

        .footer-logo {
            max-width: 15%;
            max-height: 15%;
        }

        .logo {
            max-width: 100%;
        }
    }
    @media screen and (min-width: 768px) and (max-width: 991px) {
        p {
            font-size: xx-small;
        }

        .footer-logo {
            max-width: 10%;
            max-height: 10%;
        }

        img {
            max-width: 12%;
        }
    }
</style>
