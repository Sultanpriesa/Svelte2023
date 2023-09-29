<svelte:head>
    <link rel="stylesheet" href="css\main.css"/>
</svelte:head>

<script>
    import Header from "$lib/Header.svelte"
    import Footer from "$lib/Footer.svelte"
</script>
   
<nav>
    <ul> 
        <li>
            <a href="/">Home</a>
        </li>
        <li>
            <a href="/About">About</a>
        </li>
        <li>
            <a href="/Team">Team</a>
        </li>
        <li>
            <a href="/Contact">Conact</a>
        </li>
    </ul>
</nav>

<Header />
<slot />
<Footer />