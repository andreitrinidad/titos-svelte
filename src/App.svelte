<script>
  let thisYear = new Date().getFullYear();
  let scrolled = false;

  function scrollIt(e) {
    e.preventDefault();
    e.target.scrollTop > 50 ? scrolled = true : scrolled = false;
  }

</script>

<svelte:head>
	<title>Titos of Llano</title>
  <link href="https://fonts.googleapis.com/css2?family=Kaushan+Script&family=Roboto+Slab:wght@300;400;700&display=swap" rel="stylesheet">
</svelte:head>


<main>
	<nav class="navigation {scrolled && 'scrolled'}">
		<a href="#" class="logo">
			<img src="./images/logo.svg" alt="">
			<div class="logo__text">Titos of Llano</div>
		</a>
		<ul class="links">
			<li><a href="#mission-vision">Mission x Vision</a></li>
			<li><a href="#titos">The titos</a></li>
      <li><a href="#about">Who we are</a></li>
		</ul>
	</nav>

  <div class="maincontainer" on:scroll={ scrollIt }>
 
	<section class="landing">
    <div class="landing__logo">
      <h1>
        <span>
          <h2>We are</h2>
          Titos of Llano.
          <h3>A non-profit organization™</h3>
        </span>
      </h1>
      <img src="./images/mustache.svg" alt="">
    </div>

    <div class="landing__scroll">
      <img src="./images/arrow-down.svg" alt="">
      <p>scroll</p>
    </div>
	</section>
 

  <section class="mv" id="mission-vision">
    <div class="mv-container">
      <div class="mv-wrapper">
        <h2 class="h2-display">Mission</h2>
        <div class="mv-text-container">
          Bacon ipsum dolor amet venison meatloaf pork chop prosciutto short loin porchetta rump cupim. Venison brisket turkey, leberkas sausage cupim kevin short loin drumstick ham capicola ham hock corned beef tenderloin bacon. Drumstick prosciutto ground round burgdoggen filet mignon. Pork chop salami pastrami capicola kielbasa sirloin meatloaf chislic pork loin. Buffalo t-bone burgdoggen tri-tip shankle, tenderloin filet mignon.
        </div>
      </div>
    </div>
    <div class="mv-container mv-container--right">
      <div class="mv-wrapper">
        <h2 class="h2-display">Vision</h2>
        <div class="mv-text-container">
          Bacon ipsum dolor amet venison meatloaf pork chop prosciutto short loin porchetta rump cupim. Venison brisket turkey, leberkas sausage cupim kevin short loin drumstick ham capicola ham hock corned beef tenderloin bacon. Drumstick prosciutto ground round burgdoggen filet mignon. Pork chop salami pastrami capicola kielbasa sirloin meatloaf chislic pork loin. Buffalo t-bone burgdoggen tri-tip shankle, tenderloin filet mignon.
        </div>
      </div>
    </div>
  </section>

  <section class="titos" id="titos">
    <h1>The Titos</h1>
    <p>We are at our prime age—the 20s in which we feel the existential crisis the most.</p>
    <div class="titos__container">
      <figure>
        <img src="./images/tito1.png" alt="">
        <figcaption>
          <a href="#" id="">
            Kenn Palma
          </a>
        </figcaption>
      </figure>
      <figure>
        <img src="./images/tito2.png" alt="">
        <figcaption>
          <a href="#" id="">
            Rey Bersabal
          </a>
        </figcaption>
      </figure>
      <figure>
        <img src="./images/tito4.png" alt="">
        <figcaption>
          <a href="#" id="">
            Andrei Trinidad
          </a>
        </figcaption>
      </figure>
      <figure>
        <img src="./images/tito3.png" alt="">
        <figcaption>
          <a href="#" id="">
            Mark Bernardo
          </a>
        </figcaption>
      </figure>
    </div>

  </section>

  <section class="about" id="about">
    <hr>
    <h2>About us</h2>
    <p>
      Bacon ipsum dolor amet venison meatloaf pork chop prosciutto short loin porchetta rump cupim. Venison hrisket turkey, leberkas sausage cupim kevin short loin drumstick ham capicola ham hock corned beef tenderloin bacon. Drumstick prosciutto ground round burgdoggen filet mignon. Pork chop salami pastrami capicola kielbasa sirloin meatloaf chislic pork loin. Buffalo t-bone burgdoggen tri-tip shankle, tenderloin filet mignon.
    </p>
    <hr>
    <h2>Socials</h2>
    <div>
      <a href="#"><img src="./images/fb.svg" alt=""></a>
      <a href="#"><img src="./images/ig.svg" alt=""></a>
      <a href="#"><img src="./images/tw.svg" alt=""></a>
    </div>
    <hr>
  </section>
  <footer>
    <div class="wrapper">
      <p>Titos of Llano &copy; All Rights Reserved {thisYear}</p>
      <p>a site by <a href="https://fb.me/ughndrei">andreitrinidad</a></p>
    </div>
  </footer>
  </div>



</main>

<style type="text/scss">
  @import './scss/breakpoint';
  @import './scss/variables';
  
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
    scroll-behavior: smooth;
  }

  :global(html) {
    // scroll-behavior: smooth;
  }
  
  a {
    text-decoration: none;
    color: unset;
  }


  @import './scss/main';

  footer {
    width: 100%;
    @include font-text(12);
    background-color: $whitish-white;

    .wrapper {
      display: flex;
      justify-content: space-between;  
      margin: 0 auto;
      max-width: 1280px;
      padding: 10px 30px;
    }

    a {
      &:hover{
       text-decoration: underline;
      }
    }

    p:last-of-type {
      text-align: right;
    }
  }
</style>
