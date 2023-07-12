<script>
    import fondo_proyecte from "$lib/img/fondo_proyecte.png"
    import fondo_gris from "$lib/img/Fondo_gris_projecte.png"
</script>
<section>
    <div class="fondo_proyecte">
        <img src={fondo_proyecte} alt="fondo_proyecte">
    </div>

    <div class="fondo_gris">
        <img src={fondo_gris} alt="fondo_proyecte">
    </div>

    <div class="fondo_texto">
        <h2>El Nostre Proyecte</h2>
        <p>L’Espai Musical de Moià (EMM) és una cooperativa sense ànim de lucre que té com a objectiu principal
            democratitzar la pràctica musical i artística de Moià i el Moianès. La participació dels socis i els seus
            interessos musicals i artístics són el motor de creixement i desenvolupament de l’EMM. És un projecte
            innovador i jove, creat per un grup de pedagogs musicals que sentien la necessitat de promoure l’activitat
            musical a la població de Moià i la seva comarca.
            L’EMM segueix dues línies d’acció:
            Com a facilitador d’un espai d’aprenentatge musical, obert a totes les edats i nivells i amb unes polítiques
            econòmiques de gran abast.</p><br>
        <h3> Tothom ha de tenir accés a la música i l’art, eines indispensables per al desenvolupament personal i
            social</h3>
        <p>Com a organitzador i promotor de concerts i esdeveniments musicals públics, per ell mateix o fent xarxa amb
            altres entitats i agrupacions:</p>
        <h3>Volem una comarca rica en cultura on les arts tinguin un paper central</h3>
    </div>
</section>

<style>
    section {
        position: relative;
        display: inline-block;
        text-align: center;
    }

    .fondo_proyecte {
        display: flex;
        position: absolute;
        width: auto;
    }

    .fondo_gris {
        display: flex;
        position: relative;
        margin-left: 120px;
    }

    .fondo_texto {
        display: flex;
        position: absolute;
        flex-wrap: wrap;
        top: 720px;
        justify-content: space-evenly;
    }

    p {
        margin-inline-start: 220px;
        margin-inline-end: 150px;
    }

</style>