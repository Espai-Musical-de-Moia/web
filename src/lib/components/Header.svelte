<script>
    import {goto} from '$app/navigation';
    import {page} from '$app/stores';
    import logo from "$lib/img/logo.png";

    function handleButtonClick() {
        goto('/inscripcio');
    }
</script>

    <header>
        <img src={logo} alt="header-logo"/>
        <nav>
            <ul>
                <li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
                    <a href="/">Projecte</a>
                </li>
                <li aria-current={$page.url.pathname === '/horaris' ? 'page' : undefined}>
                    <a href="/horaris">Horari</a>
                </li>
                <li aria-current={$page.url.pathname === '/espectacles' ? 'page' : undefined}>
                    <a href="/espectacles">Espectacles</a>
                </li>
                <li aria-current={$page.url.pathname === '/calendari' ? 'page' : undefined}>
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
    img{
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
    }

    nav {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
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

    li[aria-current="page"] {
        background-color: rgba(128, 128, 128, 0.597);
    }

</style>
