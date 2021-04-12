<script>
  export let content;
</script>

<section>
  <div class="bg-image">
    <img src="/img/bg_steps_mobile.png" alt="" />
  </div>

  <div class="container">
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
    font-weight: 700;
    line-height: 1.75rem;
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
    width: 4rem;
    height: 3rem;
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
    font-size: 1.45rem;
    padding-right: 2rem;
    line-height: 1.5rem;
  }

  .content-single p {
    font-size: 0.75rem;
    line-height: 1.5rem;
  }
</style>
