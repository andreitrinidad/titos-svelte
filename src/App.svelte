<script>
	export let name;
</script>

<svelte:head>
	<title>Titos of Llano</title>
  <link href="https://fonts.googleapis.com/css2?family=Kaushan+Script&family=Roboto+Slab:wght@300;400;700&display=swap" rel="stylesheet">
</svelte:head>

<main>
	<nav class="navigation">
		<a href="#" class="logo">
			<img src="./images/logo.svg" alt="">
			<div class="logo__text">Titos of Llano</div>
		</a>
		<ul class="links">
			<li><a href="#">Our mission</a></li>
			<li><a href="#">Our vision</a></li>
			<li><a href="#">Who we are</a></li>
			<li><a href="#">The titos</a></li>
		</ul>
	</nav>
	<section class="landing">
    <div class="landing__logo">
      <h1>
        <span>
          <h2>We are</h2>
          Titos of Llano
          <h3>A non-profit organization™</h3>
        </span>
      </h1>
      <img src="./images/mustache.svg" alt="">
    </div>
    <div class="landing__scroll">
      Under maintenance. Come back again soon!
    </div>
	</section>
</main>

<style type="text/scss">
  @import './scss/breakpoint';
  
  // variables
  $yellow: #F8EFE0;
  $yellowish: #FFFAF1;
  $white: #fff;
  $whitish-white: #F5F5F5;
  $just-black: #3B444B;
  $not-so-black: #414A4C;
  $grey: #707070;
  $lesser-grey: #B1B4B7;

  @mixin font-display($size: 12px, $weight: normal) {
    font-family: 'Kaushan Script', cursive;
    font-size: #{$size}px;
    font-weight: $weight;
  }

  @mixin font-text($size: 12px, $weight: normal) {
    font-family: 'Roboto Slab', serif;
    font-size: #{$size}px;
    font-weight: $weight;
  }

  // global things
	:global(body), * {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
  }
  
  a {
    text-decoration: none;
    color: unset;
  }



  @import './scss/main';
</style>