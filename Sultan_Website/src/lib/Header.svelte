<!-- header that will display on all page -->
<header class="header-wrap">
    <div class="container">
        <!-- F1 logo -->
        <!-- svelte-ignore a11y-img-redundant-alt -->
        <img class="header-image" 
        src="https://seeklogo.com/images/F/fia-formula-one-world-championship-logo-315707FDD7-seeklogo.com.png"
        alt="Formula 1 image">
    </div>
    <!-- Navigation part of the header sitting on the right side -->
    <div class="menu">
        <nav>
            <ul class="menu-contents"> 
                <li>
                    <a href="/home">Home</a>
                </li>
                <li>
                    <a href="/Teams">Teams</a>
                </li>
                <li>
                    <a href="/about">About</a>
                </li>
            </ul>
        </nav>
    </div>
</header>

<style>
.header-wrap{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    background-color: lightgray;
    padding: 10px;
    box-shadow:darkgray ;
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
    max-width: 2000px;
    justify-content: flex-end;
}
.menu-contents{
    display: inline-flex;
    text-align: right;
}
.menu-contents a{
    color: red;
    font-size: 45px;
    text-decoration: none;
    text-transform: uppercase;
    padding: 10px;
    margin: 10px;
    position: relative;
    transition: all .5s;
}
.menu-contents a:hover{
    background-color: rgb(231, 19, 19);
    color: rgb(17, 16, 16);
}

.menu-contents a::before{
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
.menu-contents a::after{
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
.menu-contents a:hover::before{
    opacity: 1;
    bottom: -8px;
    left: -8px;
}
.menu-contents a:hover::after
    {
    opacity: 1;
    bottom: -8px;
    left: -8px;
}
    </style>