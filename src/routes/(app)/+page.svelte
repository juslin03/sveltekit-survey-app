<script>
	import welcome from '$lib/images/svelte-welcome.webp';
	import welcome_fallback from '$lib/images/svelte-welcome.png';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>
<div>
	<div id="myCarousel" class="carousel slide" data-bs-ride="carousel">
		<div class="carousel-indicators">
		<button type="button" data-bs-target="#myCarousel" data-bs-slide-to="0" class="active" aria-current="true"
			aria-label="Slide 1"></button>
		<button type="button" data-bs-target="#myCarousel" data-bs-slide-to="1" aria-label="Slide 2"></button>
		<button type="button" data-bs-target="#myCarousel" data-bs-slide-to="2" aria-label="Slide 3"></button>
		</div>
		<div class="carousel-inner">
		<div class="carousel-item active">
			<img class="bd-placeholder-img" width="100%" height="70%" src="/images/rectanglesmile.jpg" aria-hidden="true"
			alt="nothing">
			<rect width="100%" height="100%" fill="#777" />

			<div class="container">
			<div class="carousel-caption ">
				<h1>Dis moi tes combats je te dirai qui tu es.</h1>
				<p>Prêt !? Çà démarre maintenant !</p>
				<p><a class="btn btn-lg btn-primary" href="/inscription">Inscris toi aujourd'hui</a></p>
			</div>
			</div>
		</div>
		<div class="carousel-item">
			<img class="bd-placeholder-img" width="100%" height="70%" src="/images/women.jpg" aria-hidden="true"
			alt="nothing">
			<rect width="100%" height="70%" fill="#777" />

			<div class="container">
			<div class="carousel-caption">
				<h1> Découvre ton vrai Moi !</h1>
				<p> Réponx avec honnêteté meme si les réponses ne te plaisent pas.</p>
				<p> <a class="btn btn-lg btn-primary" href="/connexion">Démarre maintenant</a> </p>
			</div>
			</div>
		</div>
		<div class="carousel-item">
			<img class="bd-placeholder-img" width="100%" height="70%" src="/images/awoman.jpg" aria-hidden="true"
			alt="nothing">
			<rect width="100%" height="70%" fill="#777" />

			<div class="container">
			<div class="carousel-caption ">
				<h1>Sois toi!</h1>
				<p>çà ne dure que 15 minutes.</p>
				<p><a class="btn btn-lg btn-primary" href="about">A propos de nous</a></p>
			</div>
			</div>
		</div>
		</div>
		<button class="carousel-control-prev" type="button" data-bs-target="#myCarousel" data-bs-slide="prev">
		<span class="carousel-control-prev-icon" aria-hidden="true"></span>
		<span class="visually-hidden">Previous</span>
		</button>
		<button class="carousel-control-next" type="button" data-bs-target="#myCarousel" data-bs-slide="next">
		<span class="carousel-control-next-icon" aria-hidden="true"></span>
		<span class="visually-hidden">Next</span>
		</button>
	</div>


	<!-- Marketing messaging and featurettes

	<div class="container marketing">
		<!-- Three columns of text below the carousel -->
	<div class="row">
		<div class="col-lg-4">
			<img class="bd-placeholder-img rounded-circle" width="140" height="140" src="/images/smilewoman.jpg"
				aria-label="Placeholder: " alt="nothing">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#777" /><text x="50%" y="50%" fill="#777" dy=".3em"></text>
			<h2 class="fw-normal">Conscience émotionnelle</h2>
			<p>La conscience émotionnelle est la capacité de reconnaître et de comprendre ses propres émotions ainsi que celles des autres.
				Une bonne conscience émotionnelle contribue à une bonne santé mentale.
			</p>
			<p><a class="btn btn-secondary" href="questionun">Fais l'état de tes émotions &raquo;</a></p>
		</div>

		<div class="col-lg-4">
			<img class="bd-placeholder-img rounded-circle" width="140" height="140" src="/images/sadman.jpg"
			aria-label="Placeholder:" alt="nothing">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#777" /><text x="50%" y="50%" fill="#777" dy=".3em"></text>
			<h2 class="fw-normal">Expression émotionnelle</h2>
			<p>L'expression émotionnelle désigne l'ensemble des traits comportementaux par lesquels se révèle l'émotion,
			tels que le sourire, les pleurs, les mimiques faciales et les attitudes.
			</p>
			<p><a class="btn btn-secondary" href="questiondeux">Fais l'état de tes émotions &raquo;</a></p>
		</div>



		<div class="col-lg-4">
			<img class="bd-placeholder-img rounded-circle" width="140" height="140" src="/images/hungryman.jpg"
			aria-label="Placeholder:" alt="ok">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#777" /><text x="50%" y="50%" fill="#777" dy=".3em"></text>
			<h2 class="fw-normal">Compréhension émotionnelle</h2>
			<p>La compréhension émotionnelle c'est le fait de comprendre le processus émotionnel, faire des liens entre l’émotion, la situation,
			l’évaluation subjective et les besoins aussi bien pour soi que pour les autres. </p>
			<p><a class="btn btn-secondary" href="questiontrois">Fais l'état de tes émotions &raquo;</a></p>
		</div>

		<div class="col-lg-4">
			<img class="bd-placeholder-img rounded-circle" width="140" height="140" src="/images/girljpg.jpg"
			aria-label="Placeholder: " alt="nothing">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#777" /><text x="50%" y="50%" fill="#777" dy=".3em"></text>
			<h2 class="fw-normal">Maitrise émotionnelle</h2>
			<p>La maîtrise de soi émotionnelle c'est la capacité à moduler ces émotions et à rester calme face à des situations stressantes,
			négatives ou qui provoquent de fortes réactions émotionnelles. </p>
			
			<p><a class="btn btn-secondary" href="questionquatre">Fais l'état de tes émotions &raquo;</a></p>
		</div>

		<div class="col-lg-4">
			<img class="bd-placeholder-img rounded-circle" width="140" height="140" src="/images/hands.jpg"
			aria-label="Placeholder:" alt="nothing">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#777" /><text x="50%" y="50%" fill="#777" dy=".3em"></text>
			<h2 class="fw-normal">Utilisation émotionnelle</h2>
			<p>L'utilisation émotionnelle, c'est également par la mise en relation cohérente de l'état émotionnel et du choix des activités. </p>
			<p><a class="btn btn-secondary" href="questioncinq">Fais l'état de tes émotions &raquo;</a></p>
		</div>


		<div class="col-lg-4">
			<img class="bd-placeholder-img rounded-circle" width="140" height="140" src="/images/woman2.jpg"
			aria-label="Placeholder:" alt="ok">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#777" /><text x="50%" y="50%" fill="#777" dy=".3em"></text>
			<h2 class="fw-normal">L'equilibre et l'harmonie émotionnelle </h2>
			<p>L'equilibre et l'harmonie émotionnelle c'est un état de stabilité psychique qui vous permet de tout affronter, même les situations les plus incommodantes.
			Il n'est pas question de quiétude ou de je-m'en-foutisme, mais bel et bien d'harmonie entre le corps et l'esprit.</p>
			<p><a class="btn btn-secondary" href="questionsix">Fais l'état de tes émotions &raquo;</a></p>
		</div>
		</div><!-- /.row -->

						
		<hr class="featurette-divider">

	<div class="row featurette">
		<div class="col-md-7">
		<h2 class="featurette-heading fw-normal lh-1">Etes vous introverti. <span class="text-muted"> </span></h2>
		<p class="lead">L'introversion désigne l' état, ou la tendance,
			orienté par une gratification interne et le bien-être mental de l'individu concerné.
			Certains romanciers caractérisent les introvertis comme
			des individus dont l'énergie psychologique se concentre à travers la
			réflexion et qui diminue durant une interaction sociale.</p>
		</div>
		<div class="col-md-5">
		<img class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto" width="500"
			height="500" src="/images/woman1.jpg" aria-label="Placeholder: 500x500"
			alt="nothing">
		<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#eee" /><text x="50%" y="50%" fill="#aaa" dy=".3em"></text>

		</div>
	</div>
		
	<hr class="featurette-divider">
	<div class="row featurette">
		<div class="col-md-7 order-md-2">
			<h2 class="featurette-heading fw-normal lh-1">Etes vous extraverti. <span class="text-muted"></span></h2>
			<p class="lead">L'extraversion définit l'état, l'acte ou l'habitude, orientée par une gratification externe à la personnalité.
			Les individus extravertis tendent à se satisfaire des interactions sociales et à être enthousiastes, bavards, et assertifs notamment.</p>
		</div>
		<div class="col-md-5 order-md-1">
			<img class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto" width="300"
			height="300" src="/images/extrawoman.jpg" aria-label="Placeholder: 500x500"
			alt="nothing">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#eee" /><text x="50%" y="50%" fill="#aaa" dy=".3em"></text>

		</div>
		</div>

		<hr class="featurette-divider">

		<div class="row featurette">
		<div class="col-md-7">
			<h2 class="featurette-heading fw-normal lh-1">Etes vous ambiverti. <span class="text-muted"></span>
			</h2>
			<p class="lead">Vous êtes peut-être ambiverti. Médiatisé au début des années 2010,
			le terme ambiversion décrit les individus qui ne sont ni extravertis ni introvertis,
			mais plutôt un mélange des deux.
			Une personnalité flexible qui représenterait la majorité de la population.</p>
		</div>
		<div class="col-md-5">
			<img class="bd-placeholder-img bd-placeholder-img-lg featurette-image img-fluid mx-auto" width="500"
			height="500" src="/images/woman who think.jpg" aria-label="Placeholder: 500x500" alt="ok">
			<title>Placeholder</title>
			<rect width="100%" height="100%" fill="#eee" /><text x="50%" y="50%" fill="#aaa" dy=".3em"></text>



		</div>
		</div>

		<hr class="featurette-divider">
	</div>
	<div class="center btn">
		<button type="button" class="btn btn-primary btn-lg"><a class="btn btn-ask" href="question">Cliquer ici pour faire le test</button>
	</div>