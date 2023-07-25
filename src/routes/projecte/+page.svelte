<script>
    import fondo_projecte from "$lib/img/inscripcioQuota/fondo_projecte.png";
</script>

<section>
    <img src={fondo_projecte} alt="fondo_projecte"/>
    <div class="projecte">
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
        margin: auto 66px;
    }

    img {
        width: 96%;
    }

    .projecte {
        background-color: #ddddddf7;
        position: absolute;
        top: 0;
        margin: 105px 90px;
        border-radius: 15px;
    }

    h2 {
        font-size: xxx-large;
    }

    p {
        font-size: x-large;
        margin: auto 10%;
    }

    h3 {
        font-size: xx-large;
        margin: 5% 10%;
        font-style: italic;
    }

    @media only screen and (max-width: 1362px) {

        .projecte {
            margin: 10px;
            font-size: 2rem;
        }

        img {
            width: 100%;
            height: 126vh;
            background-size: cover;
        }

        h2 {
            font-size: inherit;
        }

        p {
            font-size: x-large;;
            margin: 10px 5%;
        }

        h3 {
            font-size: smaller;
            margin: 5% 5%;
        }
    }

    @media only screen and (max-width: 704px) {

        img {
            height: 185vh;
        }
        h2 {
            font-size: smaller;
        }

        p {
            font-size: x-large;
        }

        h3 {
            font-size: large;
        }
    }

    @media only screen and (max-width: 375px) {
        h2 {
            font-size: large;
        }

        p {
            font-size: small;
        }
    }
</style>