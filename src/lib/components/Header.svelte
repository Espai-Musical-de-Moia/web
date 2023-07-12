<script>
        import Button from "./Button.svelte";
        import logo from "$lib/img/logo.png";
        import fondo from "$lib/img/fondo.png";
</script>

<div class="container">
        <header>

                <div class="navbar">
                        <div class="logo">
                                <img src={logo} alt="header-logo" />
                        </div>
                        <nav>
                                <div class="nav-links">
                                        <ul>
                                                <li>
                                                        <a href="/"
                                                                >Projecte</a
                                                        >
                                                </li>
                                                <li>
                                                        <a href="/horaris"
                                                                >Horari</a
                                                        >
                                                </li>
                                                <li>
                                                        <a href="/espectacles"
                                                                >Espectacles</a
                                                        >
                                                </li>
                                                <li>
                                                        <a href="/calendari"
                                                                >Calendari</a
                                                        >
                                                </li>
                                        </ul>
                                </div>
                                <div class="nav-boton">
                                        <Button>Inscripcio i preus</Button>
                                </div>
                        </nav>
                </div>
        </header>
</div>

<style>
        header {
                width: 100%;
                display: flex;
                background-color: black;
                height: 250px;
        }
        .header-background {
                position: absolute;
        }

        .navbar {
                display: flex;
                align-items: center;
                gap: 26em;

                position: relative;
                padding-left: 50px;
                z-index: 2;
        }

        ul {
                display: flex;
                list-style: none;
                gap: 20px;
        }

        ul li a {
                text-decoration: none;
                color: aliceblue;
        }

        nav {
                display: flex;
                flex-direction: row;
                justify-content: flex-end;
        }

        .logo img {
                margin-top: 14px;
                width: 60px;
                height: 70px;
        }

        .nav-boton {
                padding-left: 20em;
        }

        nav {
                display: flex;
                flex-direction: row;
                justify-content: flex-end;
        }

        .nav-boton {
                padding-left: 20em;
        }

        .texto-principal {
                position: relative;
                z-index: 3;
                padding-right: 17em;
        }

        .boton-act {
                position: relative;
                z-index: 4;
                padding-left: 24em;
        }
</style>
