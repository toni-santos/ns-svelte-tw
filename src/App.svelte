<script>
  import Navbar from './components/Navbar.svelte';
  import SectionHeader from './components/SectionHeader.svelte';
  import ProjectGrid from './components/ProjectGrid.svelte';
  import ProjectCarousel from './components/ProjectCarousel.svelte';
  import ProjectSlideshow from './components/ProjectSlideshow.svelte';
  import FAB from './components/FAB.svelte';
  import Footer from './components/Footer.svelte';
  import {afterUpdate, beforeUpdate, onDestroy, onMount} from 'svelte';

  let innerWidth;
  let projectPromise;
  $: projects = "";
  async function getProjects() {
    const response = await fetch('https://parseapi.back4app.com/classes/Project', {
        method: 'GET',
        mode: 'cors',
        headers: {
              'X-Parse-Application-Id': 'yB953MbsVE0hvNYJLy9Udleb7uF0bwB4AWDoAuD9', 
              'X-Parse-REST-API-Key': '3TA8ugnSSIN1TB8tQNDGTudYk00i9dghfwloy84c',
        },
    });
    const response_json = await response.json();
    return response_json.results;
  }
  
  beforeUpdate(() => {
    projectPromise = getProjects();
  });

  
</script>

<svelte:window bind:innerWidth />
<div class="font-Raleway">
  <div class="absolute opacity-[40%] translate-x-[90vw] translate-y-[5%]">
    <div class="absolute scale-[1.7] rotate-[30deg]">
      <img src="./hexagon.svg" alt="HEXAGON BIG">
    </div>
    <div class="scale-[1.75] rotate-[0deg]">
      <img src="./hexagon.svg" alt="HEXAGON BIG">
    </div>
  </div>
  <Navbar/>
  <FAB/>
  <main
  class="min-h-screen max-w-screen flex flex-col items-center justify-center 
  text-[#213547] bg-gradient-to-b from-red-400 via-red-900 to-red-900 top-2 pt-20"
  >
    {#await projectPromise}
      <p class="text-white text-2xl">Loading...</p>
    {:then projects}

      <ProjectGrid projects={projects}/>
      {#if (innerWidth <= 1100)}
        <ProjectCarousel projects={projects}/>
      {:else}
        <ProjectSlideshow projects={projects}/>
      {/if}
    {/await}
  </main>
  <Footer/>
</div>
