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
        width: 47%;
        max-width: 800px;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        background-color: #FFFFFF;
        border: solid 1px lightgray;
        margin-top: 30px;
        transition: linear 1s;
    }

    @media (max-width: 732px) {
        article {
            width: 100%;
        }

    }

    article:hover {
        background-color: #b9b9b9;
    }

    p {
        font-size: 18px;
        text-align: center;
        width: 87%;
    }

    img {
        width: 100%;
        overflow: hidden;

    }

    h1 {
        width: 100%;
        color: black;
        font-weight: bold;
        text-align: center;
        font-size: 24px;
    }
</style>