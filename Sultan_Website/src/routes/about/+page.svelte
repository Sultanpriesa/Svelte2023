<script>
	// created an array for the history information 
	let f1History = [ 
	{
		year: 1950,
		event: "First F1 World Championship",
		description: "The FIA Formula One World Championship is a high-speed, premier auto racing series. It began in 1950 with the inaugural season, featuring seven races.",
		imageUrl: "https://images.squarespace-cdn.com/content/v1/52744b67e4b0782c048b666f/1554311649477-8IRDL5Q6OSB7SWEMAIN1/1950+British+GP+start.jpg?format=1500w",
	},
	{
		year: 1954,
		event: "Mercedes Dominance",
		description: "Mercedes dominated in the 1954 season, with Juan Manuel Fangio winning his second consecutive title.",
		imageUrl: "https://i.kinja-img.com/image/upload/c_fill,h_675,pg_1,q_80,w_1200/0f2fdd385a29303b34f23e1de425ed55.jpg",
	},
	{
		year: 1962,
      	event: "Graham Hill's Triumph",
      	description: "Graham Hill secured his first World Championship title in 1962, becoming the only driver to win the 'Triple Crown' of motorsport.",
      	imageUrl: "http://en.espnf1.com/PICTURES/CMS/900/959.jpg",
	},
	{
      year: 1976,
      event: "Niki Lauda's Comeback",
      description: "Niki Lauda's remarkable recovery from a near-fatal crash in 1976 and his rivalry with James Hunt became one of the most iconic moments in F1 history.",
      imageUrl: "https://static.standard.co.uk/s3fs-public/thumbnails/image/2019/05/21/03/nikilauda2105a.jpg?width=1200",
    },
	{
      year: 1988,
      event: "McLaren's Dominance",
      description: "McLaren's MP4/4 car, driven by Ayrton Senna and Alain Prost, won 15 out of 16 races in the 1988 season, showcasing their dominance.",
      imageUrl: "https://garagedreams.net/wp-content/uploads/2020/12/McLaren-MP4-4-Canada-Pal-Lannuier.jpg",
    },
	{
      year: 1994,
      event: "Ayrton Senna's Tragic Death",
      description: "The tragic death of Ayrton Senna at the San Marino Grand Prix in 1994 shocked the world and led to significant safety improvements in F1.",
      imageUrl: "https://s.france24.com/media/display/552ca688-0960-11e9-bb9c-005056a964fe/w:1280/p:16x9/AYRTON-senna.gif",
    },
    {
      year: 1997,
      event: "Hakkinen's First Title",
      description: "Mika Hakkinen secured his first World Championship title with McLaren in 1997, marking the beginning of his successful F1 career.",
      imageUrl: "https://www.f1i.com/wp-content/uploads/2017/05/mika-hakkinen-jerez-1997-e1493629748794.jpg",
    },
	{
      year: 2010,
      event: "Sebastian Vettel's Youngest World Champion",
      description: "Sebastian Vettel became the youngest Formula 1 World Champion in 2010 while driving for Red Bull Racing, securing the title at the age of 23.",
      imageUrl: "https://www.emirates247.com/polopoly_fs/1.317566.1452316302!/image/image.gif",
    },
	{
      year: 2020,
      event: "Lewis Hamilton's Record-Equaling Seventh Title",
      description: "In 2020, Lewis Hamilton equaled Michael Schumacher's record with his seventh World Championship title, cementing his status as one of the greatest F1 drivers in history.",
      imageUrl: "https://i.eurosport.com/2020/11/15/2937217-60300308-2560-1440.jpg",
    },
];
</script>

<section class="about-section">
	<h2>About Formula 1 Racing</h2>
	<p>FIA Formula One World Championship is the pinnacle of motorsport. Here are some brief history of this exciting sport:</p>

	<div class="event-container">
		<!-- for each loop to display the f1History array -->
		{#each f1Histories as f1History }
		<div class="event">
			<img src={f1History.imageUrl} alt="F1 Event">
			<div class="event-details">
				<h3>{f1History.year}: {f1History.event}</h3>
				<p>{f1History.description}</p>
			</div>
		</div>
		{/each}
	</div>
</section>

<style>
	
</style>
