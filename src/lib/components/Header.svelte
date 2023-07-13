<script>
    import { goto } from '$app/navigation';
    import { page } from '$app/stores';
    import logo from "$lib/img/logo.png";

    function handleButtonClick() {
        goto('/inscripcio');
    }
</script>

<header>
    <img src={logo} alt="header-logo" />

    <nav>
        <ul>
            <li class:current={$page.url.pathname === '/'} aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
                <a href="/">Projecte</a>
            </li>
            <li class:current={$page.url.pathname === '/horaris'} aria-current={$page.url.pathname === '/horaris' ? 'page' : undefined}>
                <a href="/horaris">Horari</a>
            </li>
            <li class:current={$page.url.pathname === '/espectacles'} aria-current={$page.url.pathname === '/espectacles' ? 'page' : undefined}>
                <a href="/espectacles">Espectacles</a>
            </li>
            <li class:current={$page.url.pathname === '/calendari'} aria-current={$page.url.pathname === '/calendari' ? 'page' : undefined}>
                <a href="/calendari">Calendari</a>
            </li>
        </ul>
    </nav>
    <button type="button" on:click={handleButtonClick}>
        Inscripcio i preus
    </button>
</header>

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
        bottom: -10px; /* Ajusta la posición vertical del triángulo */
        left: 50%;
        transform: translateX(-50%);
        width: 0;
        height: 0;
        border-left: 6px solid transparent; /* Tamaño y estilo del triángulo */
        border-right: 6px solid transparent;
        border-bottom: 10px solid orangered; /* Color del triángulo */
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
    }

</style>
