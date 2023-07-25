<script>
    export let horari;
    import seguim_treballant from '$lib/img/horaris/seguim_treballant.png';
</script>

<div class="image-container">
    <img src={seguim_treballant} alt="foto">
</div>

<div class="container">
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
</div>

<style>
    .container {
        width: 100%;
        overflow-x: auto; /* Agregar scrollbar horizontal si es necesario */
        margin-bottom: 20px; /* Agregar un espacio entre la tabla y la imagen */
        position: relative; /* Establecer posición relativa para los elementos internos */
    }

    table {
        background-color: white;
        width: 100%;
        border-collapse: collapse;
        text-align: center;
    }

    th,
    td {
        padding: 10px 20px; /* Reducir el espacio interno para dispositivos pequeños */
        border: 1px solid #fefefe;
    }

    .light-gray {
        background-color: #f2f2f2;
    }

    .dark-gray {
        background-color: #dddddd;
    }

    .image-container {
        width: 100%;
        display: flex;
        justify-content: center;
        position: absolute; /* Establecer posición absoluta para la imagen */
        top: 0; /* Alinear la imagen en la parte superior */
        left: 0; /* Alinear la imagen a la izquierda */
        z-index: 1; /* Colocar la imagen por encima de la tabla */
    }

    img {
        width: 100%;
        max-width: 400px; /* Establecer un ancho máximo para la imagen */
        border-radius: 2%;
    }

    @media only screen and (max-width: 732px) {
        table {
            font-size: 14px; /* Reducir el tamaño de fuente para dispositivos pequeños */
        }
    }
</style>

