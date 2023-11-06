<script>
  const baseUrl = `https://api.unsplash.com`;
  const id = `8zE9isClm9xnb0ledrsaXnzAQzJDep52RIsLsE44pxI`;
  import { onMount } from "svelte";
  let array = [];
  let drivers = [];
  // fetching data when the component is mounted
  onMount(async () => {
    const res = await fetch("/api/f1/data.json");
    // parsing the json file
    const data = await res.json();
    drivers = data.drivers;

    //fetching photos related to F1 from unsplash API
    let image = []
    const response = await fetch(
      `${baseUrl}/search/photos?query=f1&per_page=4&client_id=${id}`
    );
    const data2 = await response.json();
    for (let i = 0; i < data2.results.length; i++) {
      image.push(data2.results[i].urls.regular);}
    array = image
  });
</script>

<main>
  <!-- section on formula one racing -->
  <section class="top-section-title-teams">
    <div class="image-container">
      <!-- svelte-ignore a11y-img-redundant-alt -->
      <img
        src="https://images2.minutemediacdn.com/image/fetch/https%3A%2F%2Fbeyondtheflag.com%2Fwp-content%2Fuploads%2Fgetty-images%2F2022%2F06%2F1240978865.jpeg"
        alt="F1 Image/Video"
      />
    </div>
    <div class="description">
      <h1>Formula One Racing</h1>
      <p>
        Formula One, also called F1 in short, is an international auto racing
        sport. F1 is the highest level of single-seat, open-wheel and
        open-cockpit professional motor racing contest. Formula One racing is
        governed and sanctioned by a world body called the
        <br /> FIA - Fédération Internationale de l'Automobile or the International
        Automobile Federation. The name "Formula" comes from the set of rules that
        the participating cars and drivers must follow. The objective of a Formula
        1 contest is to determine the winner of a race. The driver who crosses the
        finish line first after completing a pre-determined number of laps is declared
        the winner.
      </p>
    </div>
  </section>
  <!-- section on top 5 drivers -->
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
          {#if driver.id < 6}
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
  <!-- section for fetching photos from unsplash api -->
  <section>
    <h2 class="drivers-heading">Images</h2>
    <div id="images-car">
        {#each array as ary}
            <img src={ary} />
        {/each}
    </div>

  </section>
  <!-- section on list of F1 Drivers with View More Button -->
  <section>
    <h2 class="drivers-heading">2023 F1 Drivers List</h2>
    <ul class="drivers-list">
      {#each drivers as driver}
        <li>{driver.name}</li>
      {/each}
    </ul>
    <a href="/Teams"><button class="view-more-button">View In Detail</button></a
    >
  </section>
</main>

<style>
/* css section on formula one racing  */
  .top-section-title-teams {
    display: flex;
    align-items: center;
    background-color: white;
    color: black;
    padding: 20px;
  }
  .image-container {
    width: 52%;
  }
  .image-container img {
    width: 90%;
    height: auto;
    border-radius: 12px;
  }
  .description {
    flex: 1;
    padding: 20px;
  }
  .description h1 {
    font-size: 53px;
    margin-bottom: 30px;
    text-align: center;
    background-color: lightgray;
    border-radius: 11px;
  }
  .description p {
    font-size: 24px;
    line-height: 2.1;
    color: black;
    font-style: italic;
    padding-left: 20px;
    font: bold;
    text-shadow: 1px 1px 1px black;
    border-left: 10px double red;
  }
  /* css section on top 5 drivers */
  .ranking-section {
    text-align: center;
    margin: 40px 0 40px 0;
  }
  .ranking-heading {
    font-size: 53px;
    margin-top: 10px;
    margin-bottom: 20px;
    background-color: lightgray;
    border-radius: 11px;
  }
  .ranking-table {
    margin: auto;
    width: 70%;
    border-collapse: collapse;
    table-layout: fixed;
    border: 10px double red;
  }
  th,
  td {
    padding: 15px;
    text-align: center;
    font-size: 21px;
    white-space: nowrap;
  }
  th {
    background-color: whitesmoke;
  }
  tr:nth-child(even) {
    background-color: whitesmoke;
  }
  tr:hover {
    background-color: rgba(228, 228, 228, 0.459);
  }
  /* section on list of F1 Drivers with View More Button */
  .drivers-heading {
    font-size: 53px;
    margin-top: 40px;
    margin-bottom: 10px;
    text-align: center;
    background-color: lightgray;
    border-radius: 11px;
  }
  .drivers-list {
    list-style: none;
    padding: 10px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    transition: ease-in-out all;
    animation: colorChange 3s infinite;
  }
  @keyframes colorChange {
    0%,
    100% {
      color: red;
    }
    25% {
      color: darkmagenta;
    }
    50% {
      color: crimson;
    }
    75% {
      color: orange;
    }
  }

  .drivers-list li {
    margin-bottom: 10px;
    font-size: 18px;
    position: relative;
    padding: 10px;
  }
  .view-more-button {
    background-color: red;
    color: whitesmoke;
    padding: 10px 20px;
    border: 1.3px solid gray;
    border-radius: 7px;
    cursor: pointer;
    margin: 10px auto 20px;
    display: flex;
    margin-bottom: 100px;
  }
  a {
    text-decoration: none;
  }
/* css section for fetching photos from unsplash api */
  #images-car{
    margin-top: 40px;
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
    justify-content: center;
    align-items: center;
}
 img{
    height: 500px;
    width: 99%;
    border: 2px solid black;
    border-radius: 15px;
}
img:hover{
    border: 3px solid red; 
    transition: all scale(0.2);
    transform: scale(1.01);
}
</style>
