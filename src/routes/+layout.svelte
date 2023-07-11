<script>
    import Footer from "$lib/components/Footer.svelte";
    import Header from "$lib/components/Header.svelte";
    import Hero from "$lib/components/Hero.svelte";

</script>

<Header/>
<Hero/>
<Footer/>
<slot/>

<head>
    <link rel="logoStatic" href="/static/logoStatic.jpg" />
</head>
