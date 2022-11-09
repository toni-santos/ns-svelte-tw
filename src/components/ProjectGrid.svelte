<script>
    import ProjectContainer from './ProjectContainer.svelte'
    import SectionHeader from './SectionHeader.svelte'
</script>

<SectionHeader text="Projetos"/>
<section class="grid grid-cols-3 grid-rows-[repeat(3, fill)] justify-items-center p-10 gap-6 text-white">
    <div class="flex col-span-2 row-span-1 justify-center flex-wrap flex-grow bg-red-800 p-7 gap-8 rounded-lg bg-opacity-50 backdrop-blur-lg w-[100%] border-2 border-red-500">
        <ProjectContainer title="UNI" subtitle="A FEUP no teu bolso" image_url="https://play-lh.googleusercontent.com/947VgiC4ySPiJtqMxhTDP7XuZs4UTWDtVYBsergfzM4XTbLA7mS4Xrh2lksZ28bm4nrQ"/>
    </div>
    <div class="flex col-span-1 row-span-2 justify-center flex-wrap flex-col flex-grow bg-red-800 p-7 gap-8 rounded-lg bg-opacity-50 backdrop-blur-lg border-2 border-red-500">
        <ProjectContainer title="UNI" subtitle="A FEUP no teu bolso" image_url="https://play-lh.googleusercontent.com/947VgiC4ySPiJtqMxhTDP7XuZs4UTWDtVYBsergfzM4XTbLA7mS4Xrh2lksZ28bm4nrQ"/>
    </div>
    <div class="flex col-span-2 row-span-1 justify-center flex-wrap flex-grow bg-red-800 p-7 gap-8 rounded-lg bg-opacity-50 backdrop-blur-lg w-[100%] border-2 border-red-500">
        <ProjectContainer title="UNI" subtitle="A FEUP no teu bolso" image_url="https://play-lh.googleusercontent.com/947VgiC4ySPiJtqMxhTDP7XuZs4UTWDtVYBsergfzM4XTbLA7mS4Xrh2lksZ28bm4nrQ"/>
    </div>
</section>