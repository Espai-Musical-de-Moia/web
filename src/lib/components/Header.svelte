<script>
    import { goto } from '$app/navigation';
    import logo from "$lib/img/logo.png";

    function handleButtonClick() {
        goto('/inscripcio');
    }
</script>

<div class="container">
    <header>
        <div class="navbar">
            <div class="logo">
                <img src={logo} alt="header-logo"/>
            </div>
            <nav>
                <div class="nav-links">
                    <ul>
                        <li>
                            <a href="/">Projecte</a>
                        </li>
                        <li>
                            <a href="/horaris">Horari</a>
                        </li>
                        <li>
                            <a href="/espectacles">Espectacles</a>
                        </li>
                        <li>
                            <a href="/calendari">Calendari</a>
                        </li>
                        <li>
                            <button type="button" on:click={handleButtonClick}>
                                Inscripcio i preus
                            </button>
                        </li>
                    </ul>
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
        height: 120px;
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

    nav {
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
    }

    button {
        background-color: orangered;
        padding: 0.4em;
        border: none;
        color: aliceblue;
    }

</style>
