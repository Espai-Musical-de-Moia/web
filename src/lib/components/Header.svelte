<script>
    import {goto} from "$app/navigation";
    import {page} from "$app/stores";
    import logo from "$lib/img/header/logo.png";
    import fondo from "$lib/img/header/fondo.png";

    let isMobileMenuOpen = false;

    function toggleMobileMenu() {
        isMobileMenuOpen = !isMobileMenuOpen;
    }

    function handleButtonClick() {
        goto("/inscripcio");
    }
</script>

<header>
    <div class="logo">
        <img class="header-logo" src={logo} alt="header-logo"/>
    </div>

    <nav class="main-navbar">
        <button class="mobile-menu-button" on:click={toggleMobileMenu}>☰</button>
        <ul class="main-ul">
            <li
                    class:current={$page.url.pathname === "/"}
                    aria-current={$page.url.pathname === "/" ? "page" : undefined}
            >
                <a href="/">Inici</a>
            </li>
            <li
                    class:current={$page.url.pathname === "/projecte"}
                    aria-current={$page.url.pathname === "/projecte"
                    ? "page"
                    : undefined}
            >
                <a href="/projecte">Projecte</a>
            </li>
            <li
                    class:current={$page.url.pathname === "/horari"}
                    aria-current={$page.url.pathname === "/horari"
                    ? "page"
                    : undefined}
            >
                <a href="/horari">Horari</a>
            </li>
            <li
                    class:current={$page.url.pathname === "/contractacions"}
                    aria-current={$page.url.pathname === "/contractacions"
                    ? "page"
                    : undefined}
            >
                <a href="/contractacions">Contractacions</a>
            </li>
            <li
                    class:current={$page.url.pathname === "/calendari"}
                    aria-current={$page.url.pathname === "/calendari"
                    ? "page"
                    : undefined}
            >
                <a href="/calendari">Calendari</a>
            </li>
            <button class="main-button" type="button" on:click={handleButtonClick}>
                Inscripció i quotes
            </button>
        </ul>
    </nav>


    {#if isMobileMenuOpen}
        <nav class="mobile-menu">
            <ul class="mobile-ul">
                <li
                        class:current={$page.url.pathname === "/"}
                        aria-current={$page.url.pathname === "/" ? "page" : undefined}
                >
                    <a href="/">Inici</a>
                </li>
                <li
                        class:current={$page.url.pathname === "/projecte"}
                        aria-current={$page.url.pathname === "/projecte"
                    ? "page"
                    : undefined}
                >
                    <a href="/projecte">Projecte</a>
                </li>
                <li
                        class:current={$page.url.pathname === "/horaris"}
                        aria-current={$page.url.pathname === "/horaris"
                    ? "page"
                    : undefined}
                >
                    <a href="/horaris">Horari</a>
                </li>
                <li
                        class:current={$page.url.pathname === "/contractacions"}
                        aria-current={$page.url.pathname === "/contractacions"
                    ? "page"
                    : undefined}
                >
                    <a href="/contractacions">Contractacions</a>
                </li>
                <li
                        class:current={$page.url.pathname === "/calendari"}
                        aria-current={$page.url.pathname === "/calendari"
                    ? "page"
                    : undefined}
                >
                    <a href="/calendari">Calendari</a>
                </li>
                <button type="button" on:click={handleButtonClick}>
                    Inscripció i quotes
                </button>
            </ul>
        </nav>

    {/if}
</header>

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
        max-width: 15%;
    }

    ul {
        display: flex;
        list-style: none;
        gap: 60px;
        margin-right: 100px;
        align-items: center;
    }

    ul li a {
        text-decoration: none;
        color: aliceblue;
    }

    ul li.current a::before {
        content: "";
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
        padding: 0.7em 1em;
        border: none;
        color: aliceblue;
        border-radius: 5px;
        cursor: pointer;
        font-size: small;
        padding: 10px;
        margin-top: 20px;
        margin-bottom: 20px;
        width: 129px;
        border-radius: 5px;
        cursor: pointer;
        font-size: 1.2em;
        transition: background-color 0.3s ease;
        font-family: inherit;
    }

    .img-fondo {
        width: 100%;
        margin: 0;
        object-fit: cover;
    }

    .mobile-menu-button {
        display: none;
    }

    @media (max-width: 732px) {
        ul {
            display: none;
        }
    }

    @media screen and (max-width: 575px) {

        header {
            width: 100%;
            display: flex;
            background-color: black;
            height: 20%;
            justify-content: space-between;
            align-items: center;
        }

        .main-ul li {
            display: none;
        }

        .main-button {
            display: none;
        }

        ul {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            font-size: x-small;
            gap: 20px;
            background-color: rgb(43, 52, 52);
        }

        nav {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        ul li.current a::before {
            content: "";
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
            padding: 0.4em 1.5em;
            border: none;
            color: aliceblue;
            border-radius: 5px;
            cursor: pointer;
            font-size: 8px;
        }

        .mobile-menu-button {
            display: inline;
            padding: 1em 2em;
        }
    }

    @media screen and (min-width: 576px) and (max-width: 768px) {
        ul li a {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            background-color: transparent;
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

        .header-logo {
            height: 100%;
            max-width: 10%;
        }

        ul li a {
            text-decoration: none;
            color: aliceblue;
            position: relative;
        }

        ul li.current a::before {
            content: "";
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
            padding: 0.8em 1em;
            border: none;
            color: aliceblue;
            border-radius: 5px;
            cursor: pointer;
            font-size: small;
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

