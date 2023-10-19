<header class="header-wrap">
    <div class="container">
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <img class="header-image" 
        src="https://seeklogo.com/images/F/fia-formula-one-world-championship-logo-315707FDD7-seeklogo.com.png"
        alt="Formula 1 image">
    </div>
    <div class="menu">
        <nav>
            <ul class="menu-contents"> 
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
    </div>
</header>

<style>
.header-wrapper {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    background-color: #333;
    padding: 10px;
}
.container{
    max-width: 320px;
    height: auto;
    display: block;
}
.header-image{
    padding:10px;
}
.menu{
    max-width: 1200px;
    justify-content: flex-end;
}
.menu-contents{
    display: inline-flex;
    text-align: right;
}
Nav ul li {
    margin: 5px; 
}
Nav ul li a{
    color: red;
    font-size: 35px;
    text-decoration: none;
    text-transform: uppercase;
    padding: 5px 10px;
    margin: 0px 10 px;
    position: relative;
    transition: all .5s;
}
Nav a:hover{
    background-color: rgb(231, 19, 19);
    color: rgb(17, 16, 16);
}

Nav a::before{
    content: "";
    position: absolute;
    bottom: 12px;
    left: 12px;
    height: 12px;
    width: 12px;
    border: 3px solid rgb(20, 19, 19);
    border-width: 0 0 3px 3px;
    opacity: 0;
    transition: all .3s;
}
Nav a::after{
    content: "";
    position: absolute;
    bottom: 12px;
    left: 12px;
    height: 12px;
    width: 12px;
    border: 10px solid black;
    border-width: 0 0 3px 3px;
    opacity: 0;
    transition: all .3s;
} 
Nav a:hover::before{
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