<script>
  export let content;
  export let windowWidth;
</script>

<section class="container">
  <div class="hero">
    <div class="hero-wrapper">
      <div class="hero-content">
        <h1>{content.headline}</h1>
        <p>{content.paragraph}</p>

        <button>Comment ça marche</button>
      </div>
    </div>

    <div class="hero-image">
      <img
        src={windowWidth >= 768 ? content.imageDesktop : content.imageMobile}
        alt=""
      />
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
    margin-bottom: 2rem;
    padding: 0 3rem;
  }

  .hero-content p {
    padding: 0 2rem;
  }

  .hero-content button {
    position: absolute;
    top: 100%;
    width: 11rem;
    margin-left: -5.5rem;
    margin-top: -1rem;
    left: 50%;
    background-color: #001944;
    color: white;
    text-align: center;
    border-radius: 0.5rem;
    border: none;
    padding: 0.5rem 0;
  }

  .hero-image img {
    width: 100%;
  }

  /* For 768px and higher Screen Sizes */
  @media (min-width: 768px) {
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

    .hero-content button {
      position: static;
      font-size: 0.9rem;
      top: 0;
      margin-left: 0rem;
      margin-top: 0rem;
      left: 0;
    }

    .hero-image {
      display: flex;
      justify-content: flex-end;
    }

    .hero-image img {
      width: 85%;
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

    .hero-image img {
      width: 85%;
    }
  }

  @media (min-width: 1600px) {
    .hero-image img {
      width: 75%;
    }
  }
</style>
