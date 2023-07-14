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

    article {
        display: flex;
        height: 600px;
        width: 45%;
        max-width: 580px;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        background-color: #FFFFFF;
        border: solid 1px lightgray;
    }

    p {
        font-size: 18px;
        text-align: center;
        width: 80%;
    }

    img {
        width: 100%;

    }

    h1 {
        width: 100%;
        color: black;
        font-weight: bold;
        text-align: center;
        font-size: 24px;
    }

</style>