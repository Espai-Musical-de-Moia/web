<script>
    import fondo_proyecte from "$lib/img/fondo_proyecte.png";
    import image_project from "$lib/img/Carrusel/orquestra.png"
</script>

<div>
    <img src={image_project} alt="orquestra" />
    <div class="text-principal">
        <h1>Volem una comarca rica en cultura on les</h1>
        <h1>Arts tinguin un paper central</h1>
    </div>
</div>
<section>
    <div class="fondo_proyecte">
        <img src={fondo_proyecte} alt="fondo_proyecte"/>
    </div>

    <div class="fondo_gris">
        <h2>El Nostre Projecte</h2>
        <p>
            L’Espai Musical de Moià (EMM) és una cooperativa sense ànim de lucre
            que té com a objectiu principal democratitzar la pràctica musical i
            artística de Moià i el Moianès. La participació dels socis i els
            seus interessos musicals i artístics són el motor de creixement i
            desenvolupament de l’EMM. És un projecte innovador i jove, creat per
            un grup de pedagogs musicals que sentien la necessitat de promoure
            l’activitat musical a la població de Moià i la seva comarca. L’EMM
            segueix dues línies d’acció: Com a facilitador d’un espai
            d’aprenentatge musical, obert a totes les edats i nivells i amb unes
            polítiques econòmiques de gran abast.
        </p>
        <br/>
        <h3>
            Tothom ha de tenir accés a la música i l’art, eines indispensables
            per al desenvolupament personal i social
        </h3>
        <p>
            Com a organitzador i promotor de concerts i esdeveniments musicals
            públics, per ell mateix o fent xarxa amb altres entitats i
            agrupacions:
        </p>
        <h3>
            Volem una comarca rica en cultura on les arts tinguin un paper
            central
        </h3>
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
    }

    .fondo_gris {
        display: flex;
        flex-direction: column;
        position: relative;
        width: 60%;
        background-color: #dddddd52;
        margin: 60px auto;
        border-radius: 10px;
    }

    .text-principal {
        text-align: center;
        color: white;
        }
</style>
