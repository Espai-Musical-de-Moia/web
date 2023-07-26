<script>
    let questions = [
        {id: 1, text: `de 3 a 6 anys`},
        {id: 2, text: `a partir dels 7 anys, QUOTE GENERAL`},
        {id: 3, text: `1 activitat`},
        {id: 4, text: `amic de l'Espai`}
    ];

    let selected;

    function handleSelect() {
        console.log(`Selected question ${selected.id} (${selected.text})`);
    }
</script>

<p>Tria la teva quota</p>

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


