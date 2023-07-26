<script>
    let questions = [
        {id: 1, text: `2n membre de la família`},
        {id: 2, text: `3r membre de la família`},
        {id: 3, text: `4t, 5è, 6è... membre de la família`},
        {id: 4, text: `Estudiant Escola de Música`},
        {id: 5, text: `Estudiant del grau professional del Conservatori`},
        {id: 6, text: `Família monoparental`},
        {id: 7, text: `Jubilats`}
    ];

    let selected;

    function handleSelect() {
        console.log(`Selected question ${selected.id} (${selected.text})`);
    }
</script>

<p>Descomptes per la QUOTA GENERAL: marca el teu cas
    Els descomptes, només aplicables en la QUOTA GENERAL (i vinculats als familiars de la mateixa quota),
    no són acumulables: en cas d’optar a més d’un descompte es triarà el que més beneficiï al participant.</p>

<select bind:value={selected} on:change={handleSelect}>
    {#each questions as question (question.id)}
        <option value={question}>
            {question.text}
        </option>
    {/each}
</select>

<style>
    select {
        font-family: inherit;
        font-size: medium;
        height: 30px;
        width: 30%;
        padding: 5px;
        border-radius: 5px;
        border: none;
        background-color: #f5f5f5;
        box-shadow: 0 2px 5px #0000001a;
        display: inline-block;
        vertical-align: top;
        transition: box-shadow .3s ease;
    }
</style>