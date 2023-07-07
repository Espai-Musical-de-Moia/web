<script>
    import iconMail from "$lib/img/🦆 icon _mail_.svg"
    import iconTelephone from "$lib/img/🦆 icon _telephone_.svg"
</script>

<footer>
        <div class="logo">
            <img src="../src/lib/img/logo.png" alt="logo-principal" widht="119px" height="184px">
        </div>
    <section>
        <div class="contacte">
            <p>espaimusical.moia@gmail.com</p>
            <p>+34 627949433 (Dani)</p>
            <p>+34 655333709 (Queralt)</p>
            <img src={iconMail} alt="correu">
            <img src={iconTelephone} alt="telefon">
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
    </section>
</footer>

<style>
    footer {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        background-color: #07090D;
    }

    section {
        display: flex;
        justify-content: space-evenly;
    }

    p {
        color: #FFFFFF;
    }

</style>