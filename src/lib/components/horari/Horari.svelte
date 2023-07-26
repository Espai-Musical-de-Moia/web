<script>
    export let horari;
    import seguim_treballant from "$lib/img/horaris/seguim_treballant.png";
</script>


<div class="table-container">
    <img src={seguim_treballant} alt="foto">
    <table>


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
    .table-container {

        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    table {
        background-color: white;
        border-collapse: collapse;
        text-align: center;
    }

    th,
    td {
        padding: 26px 50px;
        border: 16px solid #fefefe;
    }

    .light-gray {
        background-color: #f2f2f2;
    }

    .dark-gray {
        background-color: #dddddd;
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
        position: absolute;
        width: 40%;
    }

    /* @media only screen and (max-width: 732px) {
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
     }*/

</style>