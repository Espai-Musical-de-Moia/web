<script>
    export let horari;
    import seguim_treballant from "$lib/img/horaris/seguim_treballant.png";
</script>


<div class="image-container">
    <img src={seguim_treballant} alt="foto">
</div>

<div class="container">
    <table>
        <thead>



    <thead>

        <tr>
            <th>Hora</th>
            {#each Object.keys(horari) as dia}
                <th>{dia}</th>
            {/each}
        </tr>


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
        overflow-x: auto;
        margin-bottom: 20px;
        position: relative;
    }

    table {
        background-color: white;
        width: 100%;
        border-collapse: collapse;
        text-align: center;
    }

    th,
    td {
        padding: 10px 20px;
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
    }

    div {
        width: 100vw;
        height: 50vw;

        display: flex;
        justify-content: center;
        position: absolute;
        top: 0;
        left: 0;
        z-index: 1;
    }

    img {

        width: 100%;
        max-width: 400px;
        border-radius: 2%;
    }

    @media only screen and (max-width: 732px) {
        table {
            font-size: 14px;

            width: 50%;
            height: 30vw;
            margin-top: 10%;
            border-radius: 2%;
        }

        @media screen and (max-width: 575px) {
            div {
                width: 100vw;
                height: 50vw;
                display: flex;
                justify-content: center;
                position: relative;
                z-index: 1;
            }

            img {
                width: 50%;
                height: 30vw;
                margin-top: 10%;
                border-radius: 2%;
            }
        }
        @media screen and (min-width: 768px) and (max-width: 991px) {
            div {
                width: 100vw;
                height: 50vw;
                display: flex;
                justify-content: center;
                position: relative;
                z-index: 1;
            }

            img {
                width: 50%;
                height: 30vw;
                margin-top: 10%;
                border-radius: 2%;
            }
        }

        @media screen and (min-width: 1024px) {
            div {
                width: 100vw;
                height: 50vw;
                display: flex;
                justify-content: center;
                position: relative;
                z-index: 1;
            }

            img {
                width: 50%;
                height: 30vw;
                margin-top: 10%;
                border-radius: 2%;
            }
        }
    }

</style>