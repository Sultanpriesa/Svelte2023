<script>
  import { onMount } from "svelte";
  let teams = [];
  onMount(async () => {
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
      <p>
        Uncover all the essential information regarding this season's Formula 1
        teams, including details about the drivers, their achievements on the
        podium, the points they have accumulated, and any championship titles
        they may have secured.
      </p>
    </div>
  </div>
  <div class="team-container">
    <!-- for each itteration, it assigns the current team object to the variable 
        'team' and index of the current iteration to 'i' -->
    {#each teams as team, i (team.name)}
      <div class="team-detail-title-teams">
        <div class="team-header">
          <span class="team-rank">{i + 1}</span>
          <span class="team-points">{team.points} PTS</span>
        </div>
        <div class="horizontal-line" />
        <div class="team-name">
          <span class="team-bold">{team.name}</span>
          <img src={`${team.logo}`} alt={team.name} class="team-logo" />
        </div>
        <div class="horizontal-line" />
        <div class="team-drivers">
          <ul>
            <li>{team.driver1}</li>
            <li>{team.driver2}</li>
          </ul>
        </div>
        <img src={`${team.image}`} alt={team.name} class="last-team-image" />
      </div>
    {/each}
  </div>
</body>

<style>
  .horizontal-line {
    content: "";
    display: block;
    border-bottom: 1px solid #ccc;
    margin: 10px 0;
  }
  .title-teams {
    margin-top: 20px;
    margin-right: 25px;
    margin-left: 25px;
    border-top-right-radius: 35px;
    padding-top: 20px;
    padding-right: 20px;
    border-top: solid 10px black;
    border-right: solid 10px black;
  }
  .f1-black {
    font-size: 75px;
    padding-left: 25px;
    margin: 5px;
  }
  .mini-about-teams {
    text-align: left;
    background-color: rgba(239, 236, 236, 0.351);
    font-size: 24px;
    margin-left: 20px;
    margin-right: 25px;
    padding-top: 20px;
    padding-bottom: 20px;
    padding-left: 50px;
    border-radius: 20px;
  }
  .team-detail-title-teams {
    margin-top: 20px;
    margin-right: 25px;
    margin-left: 25px;
    border-top-right-radius: 35px;
    padding-top: 20px;
    padding-right: 20px;
    border-top: solid 2px black;
    border-right: solid 2px black;
  }
  .team-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    flex-wrap: wrap;
    padding-bottom: 100px;
  }
  .team-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .team-points {
    font-size: 40px;
    font-weight: 900;
    margin-bottom: 10px;
    font-style: italic;
  }
  .team-rank {
    font-size: 40px;
    font-weight: bold;
  }
  .team-name {
    display: flex;
    align-items: center;
    font-weight: 900;
    font-size: 32px;
    color: black;
  }
  .last-team-image {
    max-width: 50%;
    display: grid;
    margin-top: 10px;
    margin: auto;
  }
  .team-logo {
    max-width: 50px;
    margin-left: auto;
    margin-right: 10px;
    object-fit: cover;
  }
  .team-drivers ul {
    list-style: none;
    padding: 0;
    font-size: 20px;
    font-weight: 700;
  }
  .team-drivers li {
    margin: 0 10px 0 10px;
    font-weight: bold;
    font-size: 1.2em;
    color: rgb(255, 0, 0);
    text-transform: uppercase;
    letter-spacing: 2px;
    text-shadow: 1px 2px 2px rgba(0, 0, 0, 0.5);
  }
</style>
