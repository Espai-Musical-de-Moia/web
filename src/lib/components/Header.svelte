<script>
        import Button from "./Button.svelte";
        import logo from "$lib/img/logo.png";
        import fondo from "$lib/img/fondo.png";
        import Principal from "./Principal.svelte";
        
</script>

<div class="container">
        <header>
                <div class="header-background">
                        <img src={fondo} alt="header-fondo" />
                </div>

                <div class="navbar">
                        <div class="logo">
                                <img src={logo} alt="header-logo" />
                        </div>
                        <nav>
                                <div class="nav-links">
                                        <ul>
                                                <li>
                                                        <a href="/proyecto"
                                                                >Projecte</a
                                                        >
                                                </li>
                                                <li>
                                                        <a href="/horario"
                                                                >Horari</a
                                                        >
                                                </li>
                                                <li>
                                                        <a href="/espectaculos"
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
                                        <Button>Inspecio i Preus</Button>
                                </div>
                        </nav>
                </div>
        </header>
        <div class="texto-principal">
                <Principal />
        </div>

        <div class="boton-act">
                <Button>Activitats</Button>
        </div>
</div>

<style>
        header {
                width: 100%;
                display: flex;
        }
        .header-background {
                position: absolute;
                z-index: 1;
        }

        .navbar{
                display: flex;
                align-items: center;
                gap: 26em;
                
                position: relative;
                padding-left: 50px;
                z-index: 2;
        }

        ul{
                display: flex;
                list-style: none;
                gap: 20px;
              
        }
      

        ul li a{

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
        

       .nav-boton{
        padding-left: 20em;

       } 

       .texto-principal{

        position: relative;
        z-index: 3;
       }
       
</style>
