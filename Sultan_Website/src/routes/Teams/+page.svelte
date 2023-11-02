<script>
	import { onMount } from "svelte";
    let teams = [];
    onMount(async() => {
        const res = await fetch("/api/f1/data.json");
        // parsing the json file
        const data = await res.json();
        teams = data.teams;
    });

</script>


<body>
    <div class="title-teams">
        <h1 class="f1-black">F1 Teams 2023</h1>
    </div>
    <div class="mini-about-teams-container">
        <div class="mini-about-teams">
            <p>Uncover all the essential information regarding this season's Formula 1 teams, 
                including details about the drivers, their achievements on the podium, the points 
                they have accumulated, and any championship titles they may have secured.
            </p>
        </div>
    </div>

</body>





<style>
.title-teams{
    margin-top: 20px;
    margin-right: 25px;
    margin-left: 25px;
    border-top-right-radius: 35px;
    padding-top: 20px;
    padding-right: 20px;
    border-top: solid 10px black;
    border-right: solid 10px black;
}
    
.f1-black{
    font-size: 75px;
    padding-left: 25px;
    margin: 5px;
}

</style>

