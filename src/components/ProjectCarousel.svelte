<script>

    import Carousel from "svelte-carousel";
    import ProjectItem from './ProjectItem.svelte'
    import AddProject from './AddProject.svelte'
    import SectionHeader from './SectionHeader.svelte'
    export let projects;

</script>
<SectionHeader text="Projetos Arquivados"/>
<div class="max-w-[100%] px-[5%] py-10">
    <Carousel>
        {#each projects as project}
            <ProjectItem project={project}/>
        {/each}
        <AddProject />
    </Carousel>
</div>