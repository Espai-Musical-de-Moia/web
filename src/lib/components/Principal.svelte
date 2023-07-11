<script>
    export let text = "Volem una comarca rica en cultura on les";
    export let artText = "Arts tinguin un paper central";
    export let actText = "Consulta els nostres esdeveniments i activitats";
</script>

<div class="text-principal">
    <h1>{text}</h1>
    <h1 class="art">{artText}</h1>
    <p class="act">{actText}</p>
</div>

<style>
    .text-principal {
        display: flex;
        flex-direction: column;
        margin-top: 3%;
        align-items: center;
    }

    h1 {
        color: #ffffff;
        line-height: 0%;
    }

    .art {
        color: red;
        line-height: 0%;
    }

    p {
        color: #ffffff;
    }
</style>
