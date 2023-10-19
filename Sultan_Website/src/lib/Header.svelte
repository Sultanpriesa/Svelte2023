<header class="header-wrap">
    <div class="logo">
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <img class="header-image" 
        src="https://seeklogo.com/images/F/fia-formula-one-world-championship-logo-315707FDD7-seeklogo.com.png"
        alt="Formula 1 image">
    </div>
    <nav>
        <ul class="menu"> 
            <li>
                <a href="/">Home</a>
            </li>
            <li>
                <a href="/About">About</a>
            </li>
            <li>
                <a href="/features">Features</a>
            </li>
            <li>
                <a href="/Contact">Conact</a>
            </li>
        </ul>
    </nav>
</header>

<style>
    .logo{
        size: 20px;
    }
    Nav body{
        margin: 0;
        height: 100vh;
        display: flex;
        justify-content: flex;
        align-items: center;
        font-family: sans-serif;
        background-color: #08090B;
    }
    
    Nav ul
    {
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: flex-end;
        list-style-type: none;
    }
    
    
    Nav ul li {
        margin-right: 50px; 
    }
    Nav ul li a
    {
        color: rgb(218, 208, 208);
        font-size: 35px;
        text-decoration: none;
        text-transform: uppercase;
        padding: 5px 10px;
        margin: 0px 10 px;
        position: relative;
        transition: all .5s;
    }

    Nav a:hover
    {
        background-color: rgb(231, 19, 19);
        color: white;
    }
    
    Nav a::before
    {
        content: "";
        position: absolute;
        bottom: 12px;
        left: 12px;
        height: 12px;
        width: 12px;
        border: 3px solid rgb(231, 19, 19);
        border-width: 0 0 3px 3px;
        opacity: 0;
        transition: all .3s;
    }
    
    Nav a::after
    {
        content: "";
        position: absolute;
        bottom: 12px;
        left: 12px;
        height: 12px;
        width: 12px;
        border: 3px solid rgb(231, 19, 19);
        border-width: 0 0 3px 3px;
        opacity: 0;
        transition: all .3s;
    }
    
    Nav a:hover::before
    {
        opacity: 1;
        bottom: -8px;
        left: -8px;
    }
    
    Nav a:hover::after
    {
        opacity: 1;
        bottom: -8px;
        left: -8px;
    }
    </style>