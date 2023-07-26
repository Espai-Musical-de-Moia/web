<script>
    let questions = [
        {id: 1, text: `2n membre de la família`},
        {id: 2, text: `3r membre de la família`}
    ];

    let selected;

    function handleSelect() {
        console.log(`Selected question ${selected.id} (${selected.text})`);
    }
</script>

<p>Descomptes pels MENORS DE 7 ANYS: marca el teu cas
    (els descomptes, només aplicables en la QUOTA GENERAL (i vinculats als familiars de la mateixa quota),
    no són acumulables: en cas d’optar a més d’un descompte es triarà el que més beneficiï al participant)</p>

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
}
</style>
