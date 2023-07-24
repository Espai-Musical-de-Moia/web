<script>
    export let horari;
    import seguim_treballant from '$lib/img/horaris/seguim_treballant.png';
</script>


<table>
    <thead>
    <tr>
        <th>Hora</th>
        {#each Object.keys(horari) as dia}
            <th>{dia}</th>
        {/each}
    </tr>
    </thead>
    <tbody>
    {#each Object.keys(horari["Dilluns"]) as hora, index}
        <tr>
            <td class="{index % 2 === 0 ? 'light-gray' : 'dark-gray'}">{hora}</td>
            {#each Object.values(horari) as actividades}
                <td class="{index % 2 === 0 ? 'light-gray' : 'dark-gray'}">{actividades[hora]}</td>
            {/each}
        </tr>
    {/each}
    </tbody>
</table>
<div>
<img src= {seguim_treballant} alt="foto">
</div>
<style>
    table {
        background-color: white;
        width: 100%;
        border-collapse: collapse;
        position: absolute;
        text-align: center;

    }

    th,
    td {
        padding: 26px;
        border: 16px solid #fefefe;
    }

    .light-gray {
        background-color: #f2f2f2;
    }

    .dark-gray {
        background-color: #dddddd;
    }

    div {
        width: 100%;
        display: flex;
        justify-content: center;
        position: relative;
        z-index: 1;
    }

    img {
        width: 50%;
        margin-top: 8%;
        border-radius: 2%;
    }
</style>
