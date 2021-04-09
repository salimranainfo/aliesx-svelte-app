<script>
  import Header from "./comps/Header.svelte";
  import HeroArea from "./comps/HeroArea.svelte";
  import Slider from "./comps/Slider.svelte";
  import Steps from "./comps/Steps.svelte";
  import Features from "./comps/Features.svelte";
  import Footer from "./comps/Footer.svelte";

  let name = "Rubel";

  const handleClick = () => (name = "Salim");
</script>

<div>
  <Header />

  <main>
    <HeroArea />
    <Slider />
    <Steps />
    <Features />
  </main>

  <Footer />
</div>

<style>
</style>
