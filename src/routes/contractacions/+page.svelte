<script>
    import Contractacions from "$lib/components/contractacions/Contractacions.svelte";
    import bigBand from "$lib/img/contractacions/orq1.png";
    import orq2 from "$lib/img/contractacions/orq2.png";
    import org3 from "$lib/img/contractacions/org3.png";
    import orq4 from "$lib/img/contractacions/orq4.png";
    import BigEspectacleCard from "$lib/components/contractacions/BigEspectacleCard.svelte";
</script>

<div class="container">
    <div class="main-text">
        <BigEspectacleCard/>
    </div>
    <section>
        <Contractacions titulo="BIG BAND" texto="Una de les noves confeccions de l’EMM, ofereix un concert amb possibilitat de ball d’una
                           durada d’entre 1 hora i 1 hora i mitja." imagen={bigBand}/>
        <Contractacions titulo="QUINTET DE JAZZ “BON VOJAZZ" texto="L’Espai Musical té també un grup format per joves músics que interpreten estàndards de
                           jazz. El conjunt ofereix un concert distès d’1 a 2 hores, que pot acompanyar un vermut, una
                           fira o un esdeveniment." imagen={orq2}/>
        <Contractacions titulo="XARANGA" texto=" La Xaranga és un conjunt format pels joves músics del projecte i ofereix un repertori ampli
                           de versions de la música moderna més coneguda, des de bandes sonores com El Padrino Star Wars fins a música de La Pegatina, Oliver y Benji i molts més.
                           La formació es presenta en format cercavila de carrer, per animar festivitats.
                           La durada de l’actuació pot ser al voltant d’una hora o una hora i mitja." imagen={org3}/>
        <Contractacions titulo="BANDA DE CERCAVILA" texto="La Banda es presenta en un format més clàssic de banda de carrer, tipus banda valenciana, amb
                          instruments de vent i percussió. El repertori és l’òptim per a aquest tipus de conjunt: passos
                          dobles,
                          marxes i música tradicional de cercavila. Ideal per a festes populars,
                          cercaviles o per acompanyar gegants." imagen={orq4}/>
    </section>
</div>

<style>
    section {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        width: 90%;
        margin: 50px auto;
    }
</style>