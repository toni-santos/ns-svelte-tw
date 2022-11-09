<script>
  import Navbar from './components/Navbar.svelte'
  import SectionHeader from './components/SectionHeader.svelte'
  import ProjectGrid from './components/ProjectGrid.svelte'
  import ProjectSlideshow from './components/ProjectSlideshow.svelte'
</script>
<div class="font-Raleway">
  <Navbar/>
  <main
  class="min-h-screen max-w-screen flex flex-col items-center justify-center 
  text-[#213547] bg-gradient-to-b from-red-400 to-red-900 top-2 pt-20"
  >
    <ProjectGrid/>
    <ProjectSlideshow/>
  </main>
</div>
