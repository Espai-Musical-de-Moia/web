<script>
    import iconMail from "$lib/img/🦆 icon _mail_.svg"
    import iconTelephone from "$lib/img/🦆 icon _telephone_.svg"
</script>

<footer>
    <div class="logo">
        <img src="../src/lib/img/logo.png" alt="logo-principal" widht="119px" height="184px">
    </div>
    <hr>
    <section>
        <div class="contacte">
            <div class="mail">
                <img src={iconMail} alt="correu">
                <p>espaimusical.moia@gmail.com</p>
                <div class="Phone">
                    <p>+34 627949433 (Dani)</p>
                    <img src={iconTelephone} alt="telefon">
                    <p>+34 655333709 (Queralt)</p>
                </div>
            </div>

            <div class="avis">
                <p>Avís Legal</p>
                <p>Política de Cookies</p>
                <p>Política de Privacitad</p>
            </div>

            <div class="documentacio">
                <p>Protecció de Dades</p>
                <p>Documentació Responsable</p>
            </div>
        </div>
    </section>
</footer>

<style>
    footer {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        background-color: #07090D;
    }

    .logo {
        display: flex;
        justify-content: center;
        margin-bottom: 10px;

    }

    .contacte {
        display: flex;
        width: 20px;
        height: 20px;

    }

    section {
        display: flex;
        justify-content: space-evenly;
        margin-top: 20px;
    }

    p {
        color: #FFFFFF;
    }

</style>