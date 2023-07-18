<script>
    import "../app.css";
    import Footer from "$lib/components/Footer.svelte";
    import Header from "$lib/components/Header.svelte";



</script>

<div class="layout">
    <Header />
    <section>
        <slot />
        <Footer />
    </section>

</div>


<style>
    section {
        width: 100%;
        position: absolute;
        top: 170px;
    }
</style>

