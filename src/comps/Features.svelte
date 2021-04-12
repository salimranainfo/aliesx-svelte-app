<script>
  export let content;
</script>

<section>
  <div class="container">
    <div class="intro">
      <h2>{content.headline}</h2>
      <p>{content.paragraph}</p>
    </div>

    <div class="content">
      {#each content.features as feature, i}
        <div
          class="content-single"
          style="margin-bottom: {!feature.image && 0}px"
        >
          <div class="image">
            <img src={feature.image} alt="" />
          </div>

          <h3>
            <span class="bg-color" />
            <span class="number">
              <span>{i + 1}</span>
              <svg
                width="38"
                height="44"
                viewBox="0 0 38 44"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <g filter="url(#filter0_d)">
                  <path
                    d="M4 18.4545C7.15427 11.127 10.5286 7.39676 17.6364 1C25.2633 7.14685 29.0645 10.8503 34 18.4545C29.079 26.5301 25.5931 30.5404 17.6364 36.4545C10.8418 30.4864 7.55045 26.7664 4 18.4545Z"
                    fill="#BCA37D"
                  />
                </g>
                <defs>
                  <filter
                    id="filter0_d"
                    x="0"
                    y="0"
                    width="38"
                    height="43.4545"
                    filterUnits="userSpaceOnUse"
                    color-interpolation-filters="sRGB"
                  >
                    <feFlood flood-opacity="0" result="BackgroundImageFix" />
                    <feColorMatrix
                      in="SourceAlpha"
                      type="matrix"
                      values="0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 127 0"
                    />
                    <feOffset dy="3" />
                    <feGaussianBlur stdDeviation="2" />
                    <feColorMatrix
                      type="matrix"
                      values="0 0 0 0 0.904167 0 0 0 0 0.571752 0 0 0 0 0 0 0 0 0.25 0"
                    />
                    <feBlend
                      mode="normal"
                      in2="BackgroundImageFix"
                      result="effect1_dropShadow"
                    />
                    <feBlend
                      mode="normal"
                      in="SourceGraphic"
                      in2="effect1_dropShadow"
                      result="shape"
                    />
                  </filter>
                </defs>
              </svg>
            </span>
            <span class="title">
              {feature.title}
            </span>
          </h3>
          <p>{feature.details}</p>
        </div>
      {/each}
    </div>

    <div class="footer">
      <p>{content.footer}</p>
    </div>
  </div>
</section>

<style>
  .container {
    padding: 6rem 2rem;
  }

  .intro {
    text-align: center;
    padding-bottom: 3rem;
  }

  .intro h2 {
    font-weight: bold;
    margin-bottom: 2rem;
    line-height: 2rem;
    padding: 0 1rem;
  }

  .intro p {
    line-height: 1.75rem;
    padding: 0 1rem;
  }

  .content-single {
    margin-bottom: 4rem;
  }

  .content-single .number {
    display: inline-block;
    position: absolute;
    top: 0;
    left: 0;
    margin-top: -1rem;
  }

  .content-single h3 {
    position: relative;
    padding: 0.75rem 0.5rem 0.75rem 2rem;
    margin-bottom: 2rem;
  }

  .content-single h3 .bg-color {
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    background-color: #e4e7ee;
    filter: blur(5px);
    z-index: 0;
  }

  .content-single .number span {
    position: absolute;
    top: 22.5%;
    left: 37%;
    color: white;
    font-weight: bold;
  }

  .content-single h3 .title {
    z-index: 1;
    position: relative;
    font-weight: bold;
    font-size: 1.5rem;
  }

  .content-single p {
    line-height: 1.75rem;
  }

  .content-single .image {
    display: flex;
    justify-content: flex-end;
    padding: 1rem 0;
  }

  .content {
    border-bottom: 2.5px dashed #ebebeb;
  }

  .footer {
    padding: 5rem 0rem 10rem 0rem;
    text-align: center;
    line-height: 1.75rem;
  }
</style>
