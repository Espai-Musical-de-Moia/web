<script>
    import main from "$lib/img/contratacions/main.png";
</script>

<article>
    <div>
        <h1>L’ORQUESTRA DE CAMBRA DEL MOIANÈS</h1>
        <p>L’Orquestra de Cambra del Moianès és el conjunt més gran del projecte. Agrupa músics
            joves i adults de la comarca amb un alt nivell instrumental amb la intenció de preparar
            repertori simfònic de qualitat. A poc a poc, l'orquestra vol crear i esdevenir un marc musical
            de referència a la comarca, essent un atractiu pels joves músics moianesos que vulguin
            estudiar la música de manera semiprofessional o professional, oferint al mateix temps a les
            audiències de la comarca i de més enllà concerts i espectacles de qualitat, a més de seguir
            potenciant col·laboracions amb altres artistes del Moianès.</p>
    </div>

    <img src={main} alt="fotoMain">
</article>

<style>
    article {
        width: 85%;
        padding: 70px;
        margin-left: 40px;
        display: flex;
        justify-content: center;
        background-color: white;
        border:1px solid ;
        height: 280px;
        margin-top: -40px;
    }

    div {
        display: flex;
        flex-direction: column;
        max-width: 80%;
        justify-content: center;
    }

    img {
        width: 500px;
    }

    h1{
        text-align: center;
        color: black;
    }
    p{
        color: black;
        font-size:20px;
    }

    @media only screen and (max-width: 732px) {
        article {
            width: 80%;
            padding: 30px;
            display: flex;
            justify-content: center;
            background-color: white;
            border:1px solid ;
            height: 280px;
        }

        div {
            display: flex;
            flex-direction: column;
            max-width: 80%;
            justify-content: center;
        }
        img {
            width: 500px;
        }
        h1{
            text-align: center;
            color: black;
        }
        p{
            color: black;
            font-size:13px;
        }
    }
</style>