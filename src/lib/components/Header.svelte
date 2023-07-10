<script>
    import Button from "./Button.svelte";

  
</script>




<header>
        
        <div class="header-background">
                <img src="../src/lib/img/fondo.png" alt="fondo-header">
        </div>
            
        
                <div class="navbar">
                                 <img src="../src/lib/img/logo.png" alt="logo-principal" widht="50px" height="114px">
                <nav>
                        <ul>
                           
                                <li><a href="/proyecto">Projecte</a></li>
                                <li><a href="/horario">Horari</a></li>
                                <li><a href="/espectaculos">Espectacles</a></li>
                                <li><a href="/calendari">Calendari</a></li>                                       
                                  
                        
                               
                        </ul>
                                        
                </nav>
        </div>
        <Button>Inspecio i Preus</Button>


</header>


<style>

        header{
                display: flex;
                justify-content: space-between;
                align-items: center;
        }
        .header-background{
                           
                position: absolute;
                z-index: 1;
        }

        .navbar{
                display: flex;
                align-items: center;
                gap: 3em;
                position: relative;
                z-index: 2;
        }

        ul{
                display: flex;
                justify-content: space-between;
                list-style: none;
                gap: 20px;
        }
      

        ul li a{

                text-decoration: none;
                color: aliceblue;
               
        } 

       button {
        background-color: orangered;
       }
</style>
