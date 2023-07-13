<script>
    export let titulo
    export let texto
    export let imagen


</script>
<div class="orquestras">
    <h1>{titulo}</h1>
    <p> {texto}</p>
    <img src={imagen} alt="imagen">
</div>

<style>
    p {
        font-size: 23px;
        text-align: center;

    }


    .orquestras {
        width: 100%;


        display: grid;

        flex-direction: column;
        grid-gap: 30px;

    }


    img {

        width: 100%;
        height: 250px;
    }

    h1 {

        width: 100%;
        color: firebrick;
        font-weight: bold;
       text-align: center;

    }


</style>