<script>
    import Carrusel from "$lib/components/Carrusel.svelte";
    import PrincipalTop from "$lib/components/PrincipalTop.svelte";
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
