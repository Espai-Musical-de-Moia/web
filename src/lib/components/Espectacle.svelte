<script>
    export let titulo
    export let texto
    export let imagen


</script>
<article>
    <h1>{titulo}</h1>
    <p> {texto}</p>
    <img src={imagen} alt="imagen">
</article>

<style>
    p {
        font-size: 23px;
        text-align: center;

    }


    article {
        display: flex;
        width: 45%;
        flex-direction: column;
        align-items: center;
        background-color: #FFFFFF;

    }


    img {

        width: 75%;
    }

    h1 {

        width: 100%;
        color: red;
        font-weight: bold;
        text-align: center;

    }


</style>