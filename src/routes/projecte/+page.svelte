<script>
    import fondo_projecte from "$lib/img/fondo_projecte.png"
</script>

<section>
    <img src ={fondo_projecte} alt="fondo" >

    <div class="projecte">
        <h2>El Nostre Projecte</h2>
        <p>
            L’Espai Musical de Moià (EMM) és una cooperativa sense ànim de lucre que té com a objectiu principal
            democratitzar la pràctica musical i
            artística de Moià i el Moianès. La participació dels socis i els seus interessos musicals i artístics són el
            motor de creixement i
            desenvolupament de l’EMM. És un projecte innovador i jove, creat per un grup de pedagogs musicals que
            sentien la necessitat de promoure
            l’activitat musical a la població de Moià i la seva comarca. L’EMM segueix dues línies d’acció: Com a
            facilitador d’un espai
            d’aprenentatge musical, obert a totes les edats i nivells i amb unes polítiques econòmiques de gran abast.
        </p>
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
        text-align: center;
    }

    img {
        width: 80%;
        top: 10px
    }

    .projecte {
        display: flex;
        flex-direction: column;
        background-color: #ddddddc7;
        position: absolute;
        top: 0;
        margin: 45px 50px;
        width: 90%;
        border-radius: 15px;
    }

    h2 {
        font-size: xxx-large;
    }

    p {
        font-size: x-large;
        margin: auto 20%;
    }

    h3 {
        font-size: xx-large;
        margin: 5% 10%;
        font-style: italic;
    }
</style>
