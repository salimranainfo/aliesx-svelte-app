<script>
  import { onMount } from "svelte";
  import Header from "./comps/Header.svelte";
  import HeroArea from "./comps/HeroArea.svelte";
  import Slider from "./comps/Slider.svelte";
  import Steps from "./comps/Steps.svelte";
  import Features from "./comps/Features.svelte";
  import Footer from "./comps/Footer.svelte";

  import data from "../src/data.js";

  const promise = (data) => {
    return new Promise((resolve) => {
      resolve(data);
    });
  };

  let windowWidth = 0;

  onMount(() => {
    windowWidth = window.innerWidth;

    window.addEventListener("resize", () => {
      windowWidth = window.innerWidth;
    });
  });
</script>

<div>
  <Header />

  <main>
    {#await promise(data) then content}
      <HeroArea content={content.heroarea} {windowWidth} />
      <Slider content={content.slider} {windowWidth} />
      <Steps content={content.steps} {windowWidth} />
      <Features content={content.features} {windowWidth} />
    {/await}
  </main>

  <Footer />
</div>

<style>
</style>
