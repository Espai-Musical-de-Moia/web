<script>
    import main from "$lib/img/Espectacles/main.png";
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
        width: 100%;
        padding: 70px;
        display: flex;
        justify-content: center;
    }
    div {
        display: flex;
        flex-direction: column;
        max-width: 69%;
    }
    img {
        max-width: 20%;
    }
    h1{
        text-align: center;
    }
</style>