<script>
	import f1Histories from "../../lib/fetching/f1History.json"
</script>

<section class="about-section">
	<h2>About Formula 1 Racing</h2>
	<p>FIA Formula One World Championship is the pinnacle of motorsport. Here are some brief history of this exciting sport:</p>

	<div class="event-container">
		<!-- for each loop to display the f1History array -->
		{#each f1Histories.f1Histories as f1History }
		<div class="event">
			<img src={f1History.imageURL} alt="F1 Event">
			<div class="event-details">
				<h3>{f1History.year}: {f1History.event}</h3>
				<p>{f1History.description}</p>
			</div>
		</div>
		{/each}
	</div>
</section>

<style>
	.about-section{
		padding: 20px;
		text-align: center;
		font-size: 27px;
		background-color: lightgray;
	}
	.event-container > div {
		display: grid;
		grid-template-columns: 1fr 1fr;
		align-items: center;
		gap: 30px;
		margin: 30px 0 100px 0;
	}


</style>
