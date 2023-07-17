<script>
    import {goto} from '$app/navigation';
    import {page} from '$app/stores';
    import logo from "$lib/img/logo.png";
    import fondo from "$lib/img/fondo.png"

    function handleButtonClick() {
        goto('/inscripcio');
    }
</script>

<header>
    <img src={logo} alt="header-logo"/>
    <nav>
        <ul>
            <li class:current={$page.url.pathname === '/'}
                aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
                <a href="/">Inici</a>
            </li>
            <li class:current={$page.url.pathname === '/'}
                aria-current={$page.url.pathname === '/projecte' ? 'page' : undefined}>
                <a href="/">Projecte</a>
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
        </ul>
    </nav>
    <button type="button" on:click={handleButtonClick}>
        Inscripció i quotes
    </button>
</header>

<div class="img-fondo">
    <img class="img-fondo" src={fondo} alt="img-fondo"/>
</div>

<style>
    header {
        width: 100%;
        display: flex;
        background-color: black;
        height: 120px;
        justify-content: space-between;
        align-items: center;
    }

    img {
        height: 100%;
        margin-left: 40px;
        margin-top: 20px;
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
    }
</style>
