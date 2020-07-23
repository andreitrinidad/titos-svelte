<script>
	export let name;
</script>

<svelte:head>
	<title>Titos of Llano</title>
	<link href="https://fonts.googleapis.com/css2?family=Archivo+Black&display=swap" rel="stylesheet">
</svelte:head>

<main>
	<nav class="main-navigation">
		<a class="logo">
			<img src="./images/logo.svg" alt="">
			<div class="logo__text">Titos of Llano</div>
		</a>
		<ul>
			<li><a href="#">Our mission</a></li>
			<li><a href="#">Our vision</a></li>
			<li><a href="#">Who we are</a></li>
			<li><a href="#">The titos</a></li>
		</ul>
	</nav>
	<section class="landing">
	
	</section>
</main>

<style type="text/scss">
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
		p {
			color: pink;
		}
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>