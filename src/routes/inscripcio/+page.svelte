<script>
    let campo1 = '';
    let campo2 = '';
    let campo3 = '';
    let campo4 = '';
    let campo5 = '';
    let campo6 = '';
    let campo7 = '';
    let handleNext;
</script>

<h1>Inscripción</h1>

<form>
    <label>
        Cognoms, Nom (del participant):
        <input type="text" bind:value={campo1}/>
    </label>

    <label>
        Data de naixement (dia/mes/any):
        <input type="text" bind:value={campo2}/>
    </label>

    <label>
        Nom del pare, mare o tutor (si el participant és menor d'edat):
        <input type="text" bind:value={campo3}/>
    </label>

    <label>
        DNI del participant (o tutor si és menor d'edat):
        <input type="text" bind:value={campo4}/>
    </label>

    <label>
        Email:
        <input type="text" bind:value={campo5}/>
    </label>

    <label>
        Telèfon:
        <input type="text" bind:value={campo6}/>
    </label>

    <label>
        Població de residència:
        <input type="text" bind:value={campo7}/>
    </label>
</form>
<button type="button" on:click={handleNext}>Següent</button>

<style>
    form {
        display: flex;
        flex-direction: column;
        position: relative;
        width: 60%;
        background-color: #dddddd52;
        margin: 60px auto;
        border-radius: 10px;
        gap: 20px;
    }

    label {
        align-content: initial;
    }

    button {
        background-color: orangered;
        padding: 0.4em;
        border: none;
        color: aliceblue;
        margin: 2% 20%;
    }
</style>


