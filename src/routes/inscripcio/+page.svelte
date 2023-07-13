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

<div>
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
</div>


<style>
    h1 {
        margin: 30px;
    }

    div {
        background-color: #dddddd52;
    }

    form {
        display: flex;
        flex-direction: column;
        position: relative;
        width: 60%;

        margin: 60px auto;
        border-radius: 10px;
        gap: 20px;
    }

    label {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    input {
        height: 52px;
        width: 703px
    }

    button {
        background-color: orangered;
        padding: 0.4em;
        border: none;
        color: aliceblue;
        margin: 2% 20%;
        height: 52px;
        width: 203px;
        border-radius: 5px;
    }
</style>


