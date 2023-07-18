<script>
    export let horari;
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
<style>
    table {
        background-color: white;
        width: 100%;
        border-collapse: collapse;
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
</style>
