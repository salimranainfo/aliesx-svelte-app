<script>
  export let content;
  // export let windowWidth;
  import Splide from "@splidejs/splide";
  import "@splidejs/splide/dist/css/splide.min.css";

  document.addEventListener("DOMContentLoaded", function () {
    new Splide(".splide", {
      type: "loop",
      perPage: 2,
      gap: "1.5rem",
      // height: "9rem",
      cover: true,
      arrows: false,
      pagination: false,
      breakpoins: {
        640: {
          // height: "6rem",
        },
      },
    }).mount();
  });
</script>

<section class="container">
  <div class="hero">
    <div class="hero-wrapper">
      <div class="hero-content">
        <h1>{content.headline}</h1>
        <p>{content.paragraph}</p>
      </div>
    </div>

    <div id="slider">
      <div id="splide" class="splide">
        <img class="aircraft" src="/img/aircraft_slider.png" alt="" />
        <div class="splide__track">
          <ul class="splide__list">
            {#each content.images as item, i}
              <li class="splide__slide">
                <div class="slide">
                  <div style={`background-image: url(${item.url})`} />
                  <p>{item.title}</p>
                </div>
              </li>
            {/each}
          </ul>
        </div>
      </div>
    </div>
  </div>
</section>

<style>
  .hero-wrapper {
    position: relative;
  }

  .hero-content {
    position: relative;
    text-align: center;
    padding: 4rem 0;
  }

  .hero-content h1 {
    font-weight: 700;
    margin-bottom: 2rem;
    padding: 0 3rem;
  }

  .hero-content p {
    padding: 0 2rem;
  }

  #splide {
    position: relative;
  }

  .aircraft {
    position: absolute;
    bottom: 87%;
    left: 0;
  }

  .slide {
    width: 12rem;
    height: 12rem;
    padding: 1rem;
    overflow: hidden;
  }

  .slide div {
    height: 8rem;
    width: 10rem;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    border-radius: 1rem;
  }

  .slide p {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 0.75rem;
    height: 2rem;
  }

  /* For 1024px and higher Screen Sizes */
  @media (min-width: 1024px) {
    .hero-content {
      padding-top: 7rem;
      position: absolute;
      text-align: left;
      padding-left: 2rem;
      width: 22rem;
    }

    .hero-content h1 {
      padding: 0;
      padding-right: 5rem;
    }
    .hero-content p {
      padding: 0;
      margin-bottom: 2rem;
    }
  }

  @media (min-width: 1200px) {
    .hero-wrapper {
      width: 1200px;
      margin-left: auto;
      margin-right: auto;
    }

    .hero-content {
      padding-left: 0;
    }

    .hero-content h1 {
      font-size: 2rem;
    }
  }
</style>
