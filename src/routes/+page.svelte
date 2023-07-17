<script>
    import Carrusel from "$lib/components/inici/Carrusel.svelte";
    import PrincipalTop from "$lib/components/inici/PrincipalTop.svelte";
</script>

<section>
    <div>
        <PrincipalTop/>
    </div>
    <slot/>
    <div>
        <Carrusel/>
    </div>
</section>

<style>
    section {
        margin: 0;
    }
</style>
