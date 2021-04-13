<script>
  export let content;
  export let windowWidth;
  import Splide from "@splidejs/splide";
  import "@splidejs/splide/dist/css/splide.min.css";

  document.addEventListener("DOMContentLoaded", function () {
    const splide = new Splide(".splide", {
      classes: {
        arrows: "splide__arrows custom-arrows",
        arrow: "splide__arrow custom-arrow",
        prev: "splide__arrow--prev custom-prev",
        next: "splide__arrow--next custom-next",
      },
      type: "loop",
      perPage: 2,
      gap: "1.5rem",
      // height: "9rem",
      cover: true,
      arrows: true,
      pagination: false,
    }).mount();

    if (windowWidth >= 768) {
      splide.options.perPage = 4;
      splide.options.gap = "14rem";
    } else {
      splide.options.perPage = 2;
      splide.options.gap = "1.5rem";
    }

    window.addEventListener("resize", () => {
      if (windowWidth >= 768) {
        splide.options.perPage = 4;
        splide.options.gap = "14rem";
      } else {
        splide.options.perPage = 2;
        splide.options.gap = "1.5rem";
      }
    });
  });
</script>

<section class="container">
  <div class="hero">
    <div class="hero-wrapper">
      <div class="hero-content">
        <h2>{content.headline}</h2>
        <p>{content.paragraph}</p>
      </div>
    </div>

    <div id="slider">
      <div id="splide" class="splide">
        <img class="aircraft" src="/img/aircraft_slider.png" alt="" />
        <div class="splide__arrows custom-arrows">
          <span
            class="splide__arrow custom-arrow splide__arrow--prev custom-prev"
          >
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle
                cx="12"
                cy="12"
                r="12"
                transform="rotate(-180 12 12)"
                fill="#F0F0F0"
              />
              <path
                d="M8.01098 11.989C8.01052 11.7558 8.09176 11.5297 8.24058 11.3501L13.2318 5.36062C13.4013 5.15676 13.6448 5.02856 13.9087 5.00422C14.1727 4.97989 14.4355 5.06141 14.6394 5.23085C14.8432 5.40029 14.9714 5.64378 14.9958 5.90774C15.0201 6.1717 14.9386 6.43452 14.7692 6.63838L10.297 11.989L14.6094 17.3397C14.6924 17.4418 14.7543 17.5593 14.7916 17.6854C14.829 17.8115 14.8411 17.9438 14.8272 18.0745C14.8133 18.2053 14.7736 18.3321 14.7106 18.4475C14.6475 18.563 14.5622 18.6648 14.4597 18.7472C14.3571 18.8386 14.2366 18.9078 14.106 18.9506C13.9753 18.9933 13.8373 19.0086 13.7005 18.9954C13.5636 18.9823 13.431 18.9411 13.3109 18.8743C13.1907 18.8076 13.0856 18.7167 13.0022 18.6074L8.18068 12.6179C8.05539 12.4332 7.99564 12.2117 8.01098 11.989Z"
                fill="#001944"
              />
            </svg>
          </span>
          <span
            class="splide__arrow custom-arrow splide__arrow--next custom-next"
          >
            <svg
              width="24"
              height="24"
              viewBox="0 0 24 24"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <circle cx="12" cy="12" r="12" fill="#F0F0F0" />
              <path
                d="M15.989 12.011C15.9895 12.2442 15.9082 12.4703 15.7594 12.6499L10.7682 18.6394C10.5987 18.8432 10.3552 18.9714 10.0913 18.9958C9.8273 19.0201 9.56448 18.9386 9.36062 18.7692C9.15676 18.5997 9.02856 18.3562 9.00422 18.0923C8.97989 17.8283 9.06141 17.5655 9.23085 17.3616L13.703 12.011L9.39057 6.66035C9.30765 6.55824 9.24572 6.44075 9.20836 6.31463C9.17099 6.18851 9.15892 6.05625 9.17283 5.92545C9.18675 5.79465 9.22638 5.66789 9.28944 5.55245C9.3525 5.43702 9.43776 5.33519 9.54031 5.25281C9.64295 5.16139 9.76336 5.09215 9.89401 5.04943C10.0247 5.00671 10.1627 4.99144 10.2995 5.00456C10.4364 5.01768 10.569 5.05891 10.6891 5.12568C10.8093 5.19245 10.9144 5.28331 10.9978 5.39256L15.8193 11.3821C15.9446 11.5668 16.0044 11.7883 15.989 12.011Z"
                fill="#001944"
              />
            </svg>
          </span>
        </div>
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

    <div class="link">
      <a href="#!">Voir toutes les destinations</a>
    </div>
  </div>
</section>

<style>
  .container {
    padding: 3rem 0;
  }

  .hero-wrapper {
    position: relative;
    margin-bottom: 5rem;
  }

  .hero-content {
    position: relative;
    text-align: center;
  }

  .hero-content h2 {
    margin-bottom: 2rem;
    padding: 0 2rem;
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

  .custom-arrows {
    display: none;
  }

  .link {
    display: flex;
    justify-content: flex-end;
    padding-right: 2rem;
    padding-bottom: 2rem;
  }

  .link a {
    font-size: 0.75rem;
    text-decoration: underline;
    font-weight: 500;
  }

  /* For 768px and higher Screen Sizes */
  @media (min-width: 768px) {
    .hero-wrapper {
      margin-bottom: 1rem;
      margin-top: 1rem;
    }

    .hero-content {
      text-align: left;
      padding-right: 10rem;
    }

    .link {
      padding-right: 5rem;
    }

    .slide {
      width: 14rem;
      height: 12rem;
      padding: 1rem;
      overflow: hidden;
    }

    .slide div {
      height: 65%;
      width: 100%;
      background-position: center;
      background-size: 100% 100%;
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

    .custom-arrows {
      display: flex;
      justify-content: flex-end;
      padding-right: 1rem;
    }

    .custom-arrow {
      position: static;
      background-color: transparent;
    }

    .custom-prev {
      transform: rotateY(180deg) translateY(-0.95rem);
    }

    .aircraft {
      position: absolute;
      top: 75%;
      left: 0;
    }
  }

  @media (min-width: 1024px) {
    .hero-content {
      padding-right: 15rem;
    }
  }

  /* 1200px and wider devices */
  @media (min-width: 1200px) {
    .hero {
      width: 95%;
      margin-left: auto;
    }

    .hero-content h2,
    .hero-content p {
      padding-left: 0;
    }
  }

  /* 1600px and higher devices */
  @media (min-width: 1600px) {
    .hero {
      width: 80%;
    }
  }
</style>
