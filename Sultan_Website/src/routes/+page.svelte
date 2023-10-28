<script>
	import f1Histories from "../lib/fetching/f1History.json"
</script>

<main>
    <section>
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
</main>

<style>
    .image-container{
        width: 50%;
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
        font-size: 52px;
        margin-bottom: 20px;
        text-align: center;
    }
    
    
</style>