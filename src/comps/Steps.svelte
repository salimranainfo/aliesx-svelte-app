<script>
  export let content;
  export let windowWidth;
</script>

<section>
  <div class="bg-image">
    <img
      src={windowWidth >= 768
        ? "/img/bg_steps_desktop.png"
        : "/img/bg_steps_mobile.png"}
      alt=""
    />
  </div>

  <div class="container">
    <div class="wrapper">
      <h2 class="headline">{content.headline}</h2>

      <div class="content-wrapper">
        {#each content.steps as step, i}
          <div class="content-single">
            <h3>
              <span class="number">0{i + 1}</span>
              <span class="text">{step.title}</span>
            </h3>
            <p>{step.details}</p>
          </div>
        {/each}
      </div>
    </div>
  </div>
</section>

<style>
  section {
    position: relative;
  }

  .bg-image {
    width: 100%;
  }

  .bg-image img {
    width: 100%;
  }

  .container {
    width: 100%;
    padding: 7rem 2rem;
    color: white;
    position: absolute;
    top: 0;
    left: 0;
  }

  h2,
  h3 {
    color: white;
  }

  .headline {
    margin-bottom: 7rem;
    text-align: center;
  }

  .content-single {
    margin-bottom: 4rem;
  }

  .content-single h3 {
    display: flex;
    justify-content: start;
    align-items: center;
    margin-bottom: 1rem;
  }

  .content-single h3 .number {
    display: inline-block;
    width: 6rem;
    height: 4rem;
    border: 3.5px solid #6e86b0;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.75rem;
    margin-right: 1.25rem;
  }

  .content-single h3 .text {
    width: 100%;
    padding-right: 1rem;
  }

  /* For 768px and higher */

  @media (min-width: 768px) {
    .container {
      padding: 2rem 2rem;
    }

    .headline {
      margin-bottom: 2rem;
      text-align: left;
    }

    .content-single {
      margin-bottom: 2rem;
      padding-right: 15rem;
    }

    .content-single h3 {
      display: flex;
      justify-content: start;
      align-items: center;
      margin-bottom: 1rem;
    }

    .content-single h3 .number {
      width: 3.5rem;
      height: 3rem;
      font-size: 1.5rem;
      margin-right: 1.25rem;
    }

    .content-single h3 .text {
      width: 100%;
    }
  }

  /* 1024px and wider devices */
  @media (min-width: 1024px) {
    .container {
      padding: 4rem 2rem;
    }

    .headline {
      margin-bottom: 3rem;
    }

    .content-single {
      margin-bottom: 3rem;
      padding-right: 28rem;
    }

    .content-single h3 {
      display: flex;
      justify-content: start;
      align-items: center;
      margin-bottom: 1rem;
    }

    .content-single h3 .number {
      width: 3.5rem;
      height: 3rem;
      font-size: 1.5rem;
      margin-right: 1.25rem;
    }

    .content-single h3 .text {
      width: 100%;
    }
  }

  /* 1200px and wider devices */
  @media (min-width: 1200px) {
    .container .wrapper {
      width: 95%;
      margin-left: auto;
    }

    .container {
      padding: 5rem 0rem;
    }

    .headline {
      margin-bottom: 5rem;
    }

    .content-single {
      margin-bottom: 5rem;
      width: 600px;
      padding-right: 0;
    }

    .content-single h3 {
      display: flex;
      justify-content: start;
      align-items: center;
      margin-bottom: 1.5rem;
    }

    .content-single h3 .number {
      width: 5rem;
      height: 4rem;
      font-size: 1.75rem;
      margin-right: 1.25rem;
    }

    .content-single h3 .text {
      width: 100%;
      font-size: 1.75rem;
      line-height: 2rem;
    }

    .content-single p {
      font-size: 1.2rem;
      line-height: 1.75rem;
    }
  }

  /* 1600px and higher devices */
  @media (min-width: 1600px) {
    .container .wrapper {
      width: 80%;
    }

    .container {
      padding: 14rem 0rem;
    }
  }
</style>
