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
		background-color: rgb(187, 185, 185);
	}
	.event-container {
		size: 400px;
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 40px;
		margin: 30px 0 100px 0;
	}
	.event{
		text-align: center;
		max-width: 1100px;
		box-shadow: 10PX;
		background-color: lightgray;
		border-radius: 35px;
		transition: all 0.3s ease-in-out;
	}
	img{
		width: 100%;
		height: auto;
		border-top-left-radius: 35px;
		border-top-right-radius: 35px;
	}
	.event-details{
		padding: 25px;
	}
	h3 {
		margin: 0 0 10px;
		color: black;
		font-size: 35px;
	}
	p {
		font-size: 20px;
		color: black;
	}
	.event:hover{
		transform: scale(1.05);
	}

</style>
