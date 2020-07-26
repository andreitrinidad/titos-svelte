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
          The mission of the TITO’S OF LLANO (TOL) COMMUNITY ORGANIZATION, INC., has
          a tri-fold theoretical foundation; first is to serve the community in partnership with practitioners, professionals, educators, individuals (whom defined within this article as the surface-members of the organization) and the organization founders itself fore as to but not limited to engage in community-based programs and projects that will help fore as to but not limited to a. maladjusted individuals whom are members of the community or the organization itself., b. for those whom are in dire need of efficacy service or help and., c. for the citizenry of Barangay 167, Llano North Caloocan City
        </div>
      </div>
    </div>
    <div class="mv-container mv-container--right">
      <div class="mv-wrapper">
        <h2 class="h2-display">Vision</h2>
        <div class="mv-text-container">
          The main objective of the organization, pertaining to but not limited to; - increase equity and justice for those people with a limited voice in the public life; promote social equity through discourse and discussions that reflects an array of values, moral standards and social identities; engage communities and other stakeholders pertaining to, but not limited to the scope and limitations of the community area in participatory-making and policy ruling within the localities and customary sanctions of the community; create strategies that integrate collectiveness and participation among young-adult citizens of Barangay 167 Llano purposively for the pivotal value of unity; advance the right of every citizens in a socially, economically and environmentally driven community and; generate systematic ideas, projects and programs that are community-based solutions and which build local capacity that will ideally promotes the highest standard of quality-living inside the community per se.
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
      An organization composed of young adults’ citizens of Barangay. 167, Llano North Caloocan City, with passion driven perception and compassionate as a catalyst of change for the organization and the community itself. Pertaining to, but not limited to, Young Professionals of Barangay 167, with pleasing personality and lived with the spirit of leadership.
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
