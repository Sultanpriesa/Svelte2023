<script>
    import Nav from "./Nav.svelte"
</script>
<!-- <Nav /> -->

<footer>
    <div class="copyright"> 
        <span>
            This page is written by Sultan  Priesa
        </span>
        <span>
            © 2023 Sultan Priesa, All Rights reserved.
        </span>
    </div>
    <div class="footer-Button">
        <div class="button-to-top">
            <span>▲</span>
        </div>
    </div>
</footer>

<style>
footer{
    background-color: black;
    position: fixed;
    z-index: 96;
    bottom: 0;
    left: 0;
    float: none;
    width: 100%;
    box-sizing: border-box;
    justify-content: space-between;
    box-shadow: 27px 20px 15px gray;
}
.copyright{    
    font-size: 13px;
    line-height: 13px;
    float: left;
    width: auto;
    text-align: left;
    /* display: -webkit-flex; */
    flex-wrap: nowrap;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;

    color: rgb(218, 21, 21);
}
.copyright span{
    float: left;
    width: 100%;
    padding: 2px;
}

.button-to-top{
    min-width: 30px;
    height: 30px;
    margin-left: 10px;
    padding: 7px;
    
    color: white;
    

}



</style>