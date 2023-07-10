<script>
    import Button from "./Button.svelte";

  
</script>




<header>
        
        <div class="header-background">
                <img src="../src/lib/img/fondo.png" alt="fondo-header">
        </div>
            
        
                <div class="navbar">
                                 <img src="../src/lib/img/logo.png" alt="logo-principal" widht="119px" height="184px">
                <nav>
                        <ul>
                           
                                <li><a href="/proyecto">Projecte</a></li>
                                <li><a href="/horario">Horari</a></li>
                                <li><a href="/espectaculos">Espectacles</a></li>
                                <li><a href="/calendari">Calendari</a></li>
                                <Button>Inspecio i Preus</Button>                 

                               
                        </ul>
                </nav>

        </div>
        
        


</header>


<style>
        .header-background{
               
                position: absolute;
                z-index: 1;
        }

        .navbar{
                display: flex;
                justify-content: space-between;
                position: relative;
                z-index: 2;
        }

        ul{
                display: flex;
                justify-content: space-between;
                list-style: none;

        }
        ul li{
                margin-right: 20px;
               
                
        } 

        ul li a{

                text-decoration: none;
        } 

       
</style>
