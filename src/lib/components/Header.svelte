<script>
    import {goto} from '$app/navigation';
    import {page} from '$app/stores';
    import logo from "$lib/img/header/logo.png";
    import fondo from "$lib/img/header/fondo.png"

    let isMobileMenuOpen = false;

  function toggleMobileMenu() {
    isMobileMenuOpen = !isMobileMenuOpen;
  }

  function closeMobileMenu() {

    isMobileMenuOpen = false;
  }
    function handleButtonClick() {
        goto('/inscripcio');
    }
 
  
</script>

<header>
    <div class="logo">
        <img class="header-logo" src={logo} alt="header-logo"/>
     </div>
        <nav class="main-navbar">
        <ul>
            <li class:current={$page.url.pathname === '/'}
                aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
                <a href="/">Inici</a>
            </li>
            <li class:current={$page.url.pathname === '/projecte'}
                aria-current={$page.url.pathname === '/projecte' ? 'page' : undefined}>
                <a href="/projecte">Projecte</a>
            </li>
            <li class:current={$page.url.pathname === '/horari'}
                aria-current={$page.url.pathname === '/horari' ? 'page' : undefined}>
                <a href="/horari">Horari</a>
            </li>
            <li class:current={$page.url.pathname === '/contratacions'}
                aria-current={$page.url.pathname === '/contratacions' ? 'page' : undefined}>
                <a href="/contratacions">Contratacions</a>
            </li>
            <li class:current={$page.url.pathname === '/calendari'}
                aria-current={$page.url.pathname === '/calendari' ? 'page' : undefined}>
                <a href="/calendari">Calendari</a>
            </li>
        </ul>
        <button class="mobile-menu-button" on:click={toggleMobileMenu}>☰</button>
    </nav>
    <button type="button" on:click={handleButtonClick}>
        Inscripció i quotes
    </button>
</header>
    
    {#if isMobileMenuOpen}
    
    <nav class="mobile-menu">
          
        <ul>
            <li class:current={$page.url.pathname === '/'}
                aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
                <a href="/">Inici</a>
            </li>
            <li class:current={$page.url.pathname === '/projecte'}
                aria-current={$page.url.pathname === '/projecte' ? 'page' : undefined}>
                <a href="/projecte">Projecte</a>
            </li>
            <li class:current={$page.url.pathname === '/horaris'}
                aria-current={$page.url.pathname === '/horaris' ? 'page' : undefined}>
                <a href="/horaris">Horari</a>
            </li>
            <li class:current={$page.url.pathname === '/contratacions'}
                aria-current={$page.url.pathname === '/contratacions' ? 'page' : undefined}>
                <a href="/contratacions">Contratacions</a>
            </li>
            <li class:current={$page.url.pathname === '/calendari'}
                aria-current={$page.url.pathname === '/calendari' ? 'page' : undefined}>
                <a href="/calendari">Calendari</a>
            </li>
            <button type="button" on:click={handleButtonClick}>
                Inscripció i quotes
            </button>
        </ul>
    </nav>
        
  {/if}

    
<div class="img-fondo">
    <img class="img-fondo" src={fondo} alt="img-fondo"/>
</div>

<style>
    header {
        width: 100%;
        display: flex;
        background-color: black;
        height: 20%;
        justify-content: space-between;
        align-items: center;
    }
    .logo {
   margin: 2%;
    
  }
    .header-logo {
        height: 100%;
        max-width: 10%;
       
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

    ul li.current a::before {
        content: '';
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
        width: 0;
        height: 0;
        border-left: 6px solid transparent;
        border-right: 6px solid transparent;
        border-bottom: 10px solid orangered;
    }

    nav {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
    }

    button {
        background-color: orangered;
        padding: 0.8em;
        border: none;
        color: aliceblue;
        margin-right: 40px;
        border-radius: 5px;
        cursor: pointer;
        font-size: medium;
    }

    .img-fondo {
        width: 100%;
        margin: 0;
        object-fit: cover;
       
    }
    .mobile-menu-button {
    display: none;
  }
    @media screen and (max-width: 575px) {
      
       


        ul li{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        list-style: none;
        gap: 20px;
    }

    ul li a {
        text-decoration: none;
        color: aliceblue;
       
        font-size: x-small;
    }

    ul li.current a::before {
        content: '';
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
        width: 0;
        height: 0;
        border-left: 6px solid transparent;
        border-right: 6px solid transparent;
        border-bottom: 10px solid orangered;
    }

    

    button {
        background-color: orangered;
        padding: 0.2em 0.4em;
        border: none;
        color: aliceblue;
        border-radius: 5px;
        cursor: pointer;
        font-size:xx-small;
    }


    nav.mobile-menu {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-end;
      
      
  }

    .mobile-menu-button {
        display: block;
        padding: 0.7rem;
        height: 2rem;

    }
     
    
  }
  

  @media screen and (min-width: 768px) and (max-width: 991px) {

    
    button {
            display: none;
        }   
    ul {
      display: none; 
    }
    nav.mobile-menu {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: flex-end;
      position: absolute;
      top: 120px;
      right: 0;
      width: 100%;
      padding: 20px;
    }
  

    ul li {
      margin-bottom: 10px;
    }
  }
  
  @media screen and (min-width: 1024px) {

    header {
        width: 100%;
        display: flex;
        background-color: black;
        height: 20%;
        justify-content: space-between;
        align-items: center;
    }
    .logo {
   margin: 2%;
    
  }
    .header-logo {
        height: 100%;
        max-width: 10%;
       
    }

    ul {
        display: flex;
        list-style: none;
        gap: 20px;
    }

    ul li a {
        text-decoration: none;
        color: aliceblue;
        position: relative;
    }

    ul li.current a::before {
        content: '';
        position: absolute;
        bottom: -10px;
        left: 50%;
        transform: translateX(-50%);
        width: 0;
        height: 0;
        border-left: 6px solid transparent;
        border-right: 6px solid transparent;
        border-bottom: 10px solid orangered;
    }

    nav {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
    }

    button {
        background-color: orangered;
        padding: 0.8em;
        border: none;
        color: aliceblue;
        margin-right: 40px;
        border-radius: 5px;
        cursor: pointer;
        font-size: medium;
    }

    .img-fondo {
        width: 100%;
        margin: 0;
        object-fit: cover;
       
    }
    .mobile-menu-button {
    display: none;
  }
      

    }

</style>
