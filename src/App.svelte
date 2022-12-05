<script>
  import Navbar from './components/Navbar.svelte';
  import SectionHeader from './components/SectionHeader.svelte';
  import ProjectGrid from './components/ProjectGrid.svelte';
  import ProjectCarousel from './components/ProjectCarousel.svelte';
  import ProjectSlideshow from './components/ProjectSlideshow.svelte';
  import FAB from './components/FAB.svelte';
  import { onMount } from "svelte";
  import Footer from './components/Footer.svelte';
  let innerWidth;
</script>
<svelte:window bind:innerWidth />
<div class="font-Raleway">
  <div class="absolute opacity-[40%] translate-x-[90vw] translate-y-[5%]">
    <div class="absolute scale-[1.7] rotate-[25deg]">
      <img src="./hexagon.svg" alt="HEXAGON BIG">
    </div>
    <div class="scale-[1.75] rotate-[50deg]">
      <img src="./hexagon.svg" alt="HEXAGON BIG">
    </div>
  </div>
  <Navbar/>
  <FAB/>
  <main
  class="min-h-screen max-w-screen flex flex-col items-center justify-center 
  text-[#213547] bg-gradient-to-b from-red-400 via-red-900 to-red-900 top-2 pt-20"
  >
    <ProjectGrid/>
    {#if (innerWidth <= 1100)}
      <ProjectCarousel/>
    {:else}
      <ProjectSlideshow/>
    {/if}
    <Footer/>
  </main>
</div>
