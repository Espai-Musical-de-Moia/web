<script>
    import "../app.css";
    import Footer from "$lib/components/Footer.svelte";
    import Header from "$lib/components/Header.svelte";
</script>

<div class="layout">
    <Header/>
    <section>
        <slot/>
        <Footer/>
    </section>
</div>

<style>
    section {
<<<<<<< HEAD
       width: 100%; 
       position: absolute;
       top: 170px;
=======
        position: absolute;
        top: 170px;
        width: 100%;
>>>>>>> e67407c9b0d44a828bd784863b9ee748602837fc
    }
</style>
