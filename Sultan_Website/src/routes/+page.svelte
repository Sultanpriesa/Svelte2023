<script>
	import { onMount } from "svelte";
    let drivers = [];
    onMount(async() => {
        const res = await fetch("/api/f1/data.json");
        // parsing the json file
        const data = await res.json();
        drivers = data.drivers;
    });

</script>

<main>
    <section class="top-section-title-teams">
        <div class="image-container ">
            <!-- svelte-ignore a11y-img-redundant-alt -->
            <img src="https://images2.minutemediacdn.com/image/fetch/https%3A%2F%2Fbeyondtheflag.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2022%2F06%2F1240978865.jpeg" 
            alt="F1 Image/Video">
          </div>
          <div class="description ">
            <h1>Formula One Racing</h1>
            <p>
              Formula One, also called F1 in short, is an international auto racing sport. F1 is the highest level of single-seat, open-wheel 
              and open-cockpit professional motor racing contest. Formula One racing is governed and sanctioned by a world body called the
              <br/> FIA - Fédération Internationale de l'Automobile or the International Automobile Federation. The name "Formula" comes from 
              the set of rules that the participating cars and drivers must follow. The objective of a Formula 1 contest is to determine 
              the winner of a race. The driver who crosses the finish line first after completing a pre-determined number of laps is declared the winner.
            </p>
          </div>
    </section>

    <section class="ranking-section">
        <h2 class="ranking-heading">Top 5 Drivers of 2023</h2>
        <table class="ranking-table">
            <thead>
                <tr>
                    <th>Position</th>
                    <th>Name</th>
                    <th>Car</th>
                </tr>
            </thead>
            <tbody>
                {#each drivers as driver}
                {#if {id} > 6}
                <tr>
                    <td>{driver.id}</td>
                    <td>{driver.name}</td>
                    <td>{driver.car}</td>
                </tr>
                {/if}
                {/each}
            </tbody>
        </table>
    </section>


</main>

<style>
    .top-section-title-teams{
        display: flex;
        align-items: center;
        background-color: white;
        color: black;
        padding: 20px;
    }
    .image-container{
        width: 52%;
    }
    .image-container img{
        width: 90%;
        height: auto;
        border-radius: 12px;
    }
    .description{
        flex: 1;
        padding: 20px;
    }
    .description h1{
        font-size: 53px;
        margin-bottom: 30px;
        text-align: center;
        background-color: lightgray;
        border-radius: 11px;
    }
    .description p{
        font-size: 24px;
        line-height: 2.1;
        color: black;
        font-style: italic;
        padding-left: 20px;
        font: bold;
        text-shadow: 1px 1px 1px black;
        border-left: 10px double red;
    }
    .ranking-section{
        text-align: center;
        margin: 30px 0 100px 0;
    }
    .ranking-heading{
        font-size: 53px;
        margin-top: 10px;
        margin-bottom: 20px;
        background-color: lightgray;
        border-radius: 11px;
    }
    .ranking-table{
        margin:auto;
        width: 70%;
        border-collapse: collapse;
        table-layout: fixed;
        border: 10px double red;
    }
    th, td{
        padding: 15px;
        text-align: center;
        font-size: 21px;
        white-space: nowrap;
    }
    th {
        background-color: whitesmoke;
    }
    tr:nth-child(even){
        background-color: whitesmoke;
    }
    tr:hover{
        background-color: rgba(228, 228, 228, 0.459);    
    }



</style>