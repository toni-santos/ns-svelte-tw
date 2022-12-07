<script>
    import ProjectContainer from './ProjectContainer.svelte'
    import SectionHeader from './SectionHeader.svelte'
    export let projects;
</script>

<SectionHeader text="Projetos"/>
<section class="grid grid-cols-3 grid-rows-[repeat(3, fill)] justify-items-center p-10 gap-6 text-white max-lg:flex max-lg:flex-col">
    <div class="flex col-span-2 row-span-1 justify-center flex-wrap flex-grow bg-red-800 p-7 gap-8 rounded-lg bg-opacity-10 backdrop-blur-lg w-[100%] border-2 border-red-500">
        <ProjectContainer title="{projects[0].name}" subtitle="{projects[0].description}" image_url="{projects[0].imageURL}" archived="{projects[0].isArchived}" platform="{projects[0].type}"/>
    </div>
    <div class="flex col-span-1 row-span-2 justify-center flex-wrap flex-col flex-grow bg-red-800 p-7 gap-8 rounded-lg bg-opacity-10 backdrop-blur-lg border-2 border-red-500 max-lg:flex-row">
        <ProjectContainer title="{projects[3].name}" subtitle="{projects[3].description}" image_url="{projects[3].imageURL}" archived="{projects[3].isArchived}" platform="{projects[3].type}"/>
    </div>
    <div class="flex col-span-2 row-span-1 justify-center flex-wrap flex-grow bg-red-800 p-7 gap-8 rounded-lg bg-opacity-10 backdrop-blur-lg w-[100%] border-2 border-red-500">
        <ProjectContainer title="{projects[2].name}" subtitle="{projects[2].description}" image_url="{projects[2].imageURL}" archived={projects[2].isArchived} platform="{projects[2].type}"/>
    </div>
</section>