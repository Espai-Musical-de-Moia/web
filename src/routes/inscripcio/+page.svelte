<script>
    import TevaQuota from "$lib/components/inscripcioQuota/TevaQuota.svelte";
    import Descomptes7anys from "$lib/components/inscripcioQuota/Descomptes7anys.svelte";
    import DescomptesQuotaGeneral from "$lib/components/inscripcioQuota/DescomptesQuotaGeneral.svelte";
    import QuotaMensual from "$lib/components/inscripcioQuota/QuotaMensual.svelte";

  let inscripcio="";
    let campo1 = '';
    let campo2 = '';
    let campo3 = '';
    let campo4 = '';
    let campo5 = '';
    let campo6 = '';
    let campo7 = '';
    let comment = '';

    function crearID() {
        return crypto.randomUUID()
    }

    function crearInscripcio() {
        console.log('Botón "Enviar formulari" clicado.');
        let info = {
            campo1: campo1,
            campo2: campo2,
            campo3: campo3,
            campo4: campo4,
            campo5: campo5,
            campo6: campo6,
            campo7: campo7,
            comment: comment,
            id: crearID()
        };

        fetch("http://localhost:8090/", {method: "POST", body: JSON.stringify(info) })
            .then(response => response.json())
            .then(datos => inscripcio = datos)

                alert("Inscripcio Feta");
            }

</script>

<div class="container">
    <h3> US DEMANEM QUE NO FEU LA INSCRIPCIÓ SENSE ABANS HAVER CONTACTAT AMB NOSALTRES (VIA
        CORREU/TELÈFON/PERSONALMENT).<br> GRÀCIES!</h3>

    <div>
        <h2>INSCRIPCIÓ</h2>
        <form on:submit|preventDefault={crearInscripcio}>

            <div class="form-group">
                <label for="campo1">Cognoms, Nom:</label>
                <input type="text" id="campo1" bind:value={campo1} placeholder="Cognoms, Nom" required/>
            </div>

            <div class="form-group">
                <label for="campo2">Data naixement:</label>
                <input type="text" id="campo2" bind:value={campo2} placeholder="dd/mm/yyyy" required/>
            </div>

            <div class="form-group">
                <label for="campo3">Nom pare, mare o tutor:</label>
                <input type="text" id="campo3" bind:value={campo3} placeholder="Nom pare, mare o tutor" required/>
            </div>

            <div class="form-group">
                <label for="campo4">DNI participant:</label>
                <input type="text" id="campo4" bind:value={campo4} placeholder="DNI participant" required/>
            </div>

            <div class="form-group">
                <label for="campo5">Email:</label>
                <input type="text" id="campo5" bind:value={campo5} placeholder="Email" required/>
            </div>

            <div class="form-group">
                <label for="campo6">Telèfon:</label>
                <input type="text" id="campo6" bind:value={campo6} placeholder="Telèfon" required/>
            </div>

            <div class="form-group">
                <label for="campo7">Població residència:</label>
                <input type="text" id="campo7" bind:value={campo7} placeholder="Població residència" required/>
            </div>
        </form>
</div>
        <div class="formulari-quota">
            <QuotaMensual/>
            <TevaQuota/>
            <Descomptes7anys/>
            <DescomptesQuotaGeneral/>

            <p>Tens idees, aportacions, dubtes, ... digues la teva!</p>
            <textarea bind:value={comment} required></textarea>

            <button class="submit-button" on:click={crearInscripcio} disabled={!comment}>Enviar formulari</button>
        </div>
    </div>

        <style>
            .container {
                background-color: #f2f2f2;
                width: 90%;
                margin: 65px auto;
                padding: 20px;
                border-radius: 15px;
            }

            form {
                margin: 5% auto;
            }

            h2 {
                text-align: center;
                margin-bottom: 5%;
            }

            h3 {
                text-align: center;
                background-color: #ff704d;
            }

            .form-group {
                margin-bottom: 20px;
                text-align: center;
            }

            label {
                font-size: 1.3em;
                width: 30%;
                display: inline-block;
                text-align: initial;
            }

            input {
                height: 30px;
                width: 30%;
                padding: 5px;
                font-size: 1em;
                border-radius: 5px;
                border: none;
                background-color: #f5f5f5;
                box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
                display: inline-block;
                vertical-align: top;
                transition: box-shadow 0.3s ease;
            }

            input:focus {
                outline: none;
                box-shadow: 0 0 0 3px #ff6b6b;
            }

            button:hover {
                background-color: #ff704d;
            }

            .formulari-quota {
                margin: auto 10%;
                font-size: large;
                text-align: justify;
            }

            textarea {
                width: 915px;
                height: 146px;
            }

            .submit-button {
                background-color: orangered;
                padding: 10px;
                border: none;
                color: aliceblue;
                margin-top: 20px;
                margin-bottom: 20px;
                width: 300px;
                border-radius: 5px;
                cursor: pointer;
                font-size: 1.2em;
                transition: background-color 0.3s ease;
            }

            @media only screen and (max-width: 600px) {
                textarea {
                    width: 376px;
                }

                input {
                    width: 63%;
                    padding: 8px;
                }

                form {
                    width: 100%;
                    margin: 12% auto;
                    inline-size: fit-content;
                }

                .formulari-quota {
                    margin: auto;
                }
            }
        </style>