<script>
    import quotes from "$lib/img/quotes/quotes.png"
    import TevaQuota from "$lib/components/inscripcioQuota/TevaQuota.svelte";
    import Descomptes7anys from "$lib/components/inscripcioQuota/Descomptes7anys.svelte";
    import DescomptesQuotaGeneral from "$lib/components/inscripcioQuota/DescomptesQuotaGeneral.svelte";

    let campo1 = '';
    let campo2 = '';
    let campo3 = '';
    let campo4 = '';
    let campo5 = '';
    let campo6 = '';
    let campo7 = '';
    let handleNext;
    let comment = '';

    function handleSubmit() {
        // Aquí puedes enviar los datos del formulario, incluido el comentario, a través de una solicitud HTTP o realizar cualquier acción que desees.
        console.log('Submitted comment:', comment);
    }
</script>

<div class="container">
    <form>
        <h2>Datos del participante</h2>

        <div class="form-group">
            <label for="campo1">Cognoms, Nom:</label>
            <input type="text" id="campo1" bind:value={campo1} placeholder="Cognoms, Nom"/>
        </div>

        <div class="form-group">
            <label for="campo2">Data naixement:</label>
            <input type="text" id="campo2" bind:value={campo2} placeholder="dd/mm/yyyy"/>
        </div>

        <div class="form-group">
            <label for="campo3">Nom pare, mare o tutor:</label>
            <input type="text" id="campo3" bind:value={campo3} placeholder="Nom pare, mare o tutor"/>
        </div>

        <div class="form-group">
            <label for="campo4">DNI participant:</label>
            <input type="text" id="campo4" bind:value={campo4} placeholder="DNI participant"/>
        </div>

        <div class="form-group">
            <label for="campo5">Email:</label>
            <input type="text" id="campo5" bind:value={campo5} placeholder="Email"/>
        </div>

        <div class="form-group">
            <label for="campo6">Telèfon:</label>
            <input type="text" id="campo6" bind:value={campo6} placeholder="Telèfon"/>
        </div>

        <div class="form-group">
            <label for="campo7">Població residència:</label>
            <input type="text" id="campo7" bind:value={campo7} placeholder="Població residència"/>
        </div>

        <button type="button" on:click={handleNext}>Següent</button>
    </form>
</div>

<img src="{quotes}" alt="quotes">

<div class="formulari-quota">
    <TevaQuota/>
    <Descomptes7anys/>
    <DescomptesQuotaGeneral/>

    <p>Tens idees, aportacions, dubtes, ... digues la teva!</p>
    <textarea bind:value={comment}></textarea>

    <button on:click={handleSubmit} disabled={!comment}>Enviar formulario</button>
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
        width: 70%;
        margin: auto;
    }

    h2 {
        text-align: center;
        margin-bottom: 20px;
        font-size: 1.5em;
    }

    .form-group {
        margin-bottom: 20px;
    }

    label {
        font-size: 1.1em;
        width: 30%;
        display: inline-block;
        vertical-align: top;
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

    button {
        background-color: orangered;
        padding: 10px;
        border: none;
        color: aliceblue;
        margin-top: 20px;
        width: 100%;
        border-radius: 5px;
        cursor: pointer;
        font-size: 1.2em;
        transition: background-color 0.3s ease;
    }

    button:hover {
        background-color: #ff704d;
    }

    img {
        margin: auto 25%;
        width: 50%

    }

    .formulari-quota {
        margin: auto 18%;
        font-size: large;
        text-align: justify;
    }
</style>
