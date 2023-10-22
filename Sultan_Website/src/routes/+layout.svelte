<svelte:head>
    <link rel="stylesheet" href="css\main.css"/>
</svelte:head>

<script>
    import Header from "$lib/Header.svelte"
    import Footer from "$lib/Footer.svelte"
</script>
   
<Header />

<section class="Drivers-view-more-home-section">
    <div class="Drivers-view-more-home-section-box">
        <h2 class="Drivers-view-more-home-section-title">Driver Line up for 2023</h2>
    </div>
    

</section>


<slot />
<Footer />