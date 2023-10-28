<script>
	import drivers from "../lib/fetching/ranks.json"
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
        <h2>Top 5 Drivers of the season</h2>
        <table class="ranking-table">
            <thead>
                <tr>
                    <th>Position</th>
                    <th>Name</th>
                    <th>Car</th>
                </tr>
            </thead>
            <tbody>
                {#each drivers.drivers as driver (driver.id)}
                <tr>
                    <td>{driver.id}</td>
                    <td>{driver.name}</td>
                    <td>{driver.car}</td>
                </tr>
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
        font-size: 55px;
        margin-bottom: 30px;
        text-align: center;
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

</style>