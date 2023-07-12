<script>
    import main from "$lib/img/Espectacles/main.png";
    import bigBand from "$lib/img/Espectacles/orq1.png";
    import orq2 from "$lib/img/Espectacles/orq2.png";
    import org3 from "$lib/img/Espectacles/org3.png";
    import orq4 from "$lib/img/Espectacles/orq4.png";

</script>

<div class="container">

    <div class="main-text">
        <p><strong>L’ORQUESTRA DE CAMBRA DEL MOIANÈS<br></strong>

            L’Orquestra de Cambra del Moianès és el conjunt més gran del projecte. Agrupa músics
            joves i adults de la comarca amb un alt nivell instrumental amb la intenció de preparar
            repertori simfònic de qualitat. A poc a poc, l'orquestra vol crear i esdevenir un marc musical
            de referència a la comarca, essent un atractiu pels joves músics moianesos que vulguin
            estudiar la música de manera semiprofessional o professional, oferint al mateix temps a les
            audiències de la comarca i de més enllà concerts i espectacles de qualitat, a més de seguir
            potenciant col·laboracions amb altres artistes del Moianès.</p>
        <img src={main} alt="fotoMain">

    </div>
    <div class="orquestras">
    <div class="orq-1">
        <div class="text-1">
            <h1>BIG BAND</h1>
            <p>Una de les noves confeccions de l’EMM, ofereix un concert amb possibilitat de ball d’una
                durada d’entre 1 hora i 1 hora i mitja.</p>

        </div>
        <div class="img-orq1">
            <img src={bigBand} alt="orquestra1"/>
        </div>
    </div>
    <div class="orq-2">
        <p>L’Espai Musical té també un grup format per joves músics que interpreten estàndards de
            jazz. El conjunt ofereix un concert distès d’1 a 2 hores, que pot acompanyar un vermut, una
            fira o un esdeveniment.</p>
        <img src="{orq2}" alt="orquestra2"/>

    </div>

    <div class="org-3">
        <p>La Xaranga és un conjunt format pels joves músics del projecte i ofereix un repertori ampli
            de versions de la música moderna més coneguda, des de bandes sonores com El Padrino o
            Star Wars fins a música de La Pegatina, Oliver y Benji i molts més.
            La formació es presenta en format cercavila de carrer, per animar festivitats. La durada de
            l’actuació pot ser al voltant d’una hora o una hora i mitja.</p>
        <img src="{org3}" alt="orquestra3"/>

    </div>
    <div class="orq-4">
        <p>BANDA DE CERCAVILA
            La Banda es pres+enta en un format més clàssic de banda de carrer, tipus banda valenciana, amb instruments de vent i percussió. El repertori és l’òptim per a aquest tipus de conjunt: passos dobles, marxes i música tradicional de cercavila. Ideal per a festes populars,
            cercaviles o per acompanyar gegants.</p>
        <img src="{orq4}" alt="orquestra4"/>

    </div>
</div>


</div>
<style>
    .main-text {
        display: flex;
        vertical-align: baseline;
        position: relative;
        width: 100%;
        height: 350px;
    }

    p {
        font-size: 15px;
        text-align: center;
        justify-content: center;
        margin-top: 70px;
    }

    img {
        width: 30%;
        height: 300px;
        margin-top: 20px;
    }
    .orquestras{
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        grid-gap: 20px;

      }
    </style>
