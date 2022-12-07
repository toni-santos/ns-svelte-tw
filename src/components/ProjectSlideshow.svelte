<script>
    import ProjectItem from './ProjectItem.svelte';
    import SectionHeader from './SectionHeader.svelte';
    import AddProject from './AddProject.svelte';
    export let projects;

</script>

<SectionHeader text="Projetos Arquivados"/>
<section class="grid grid-cols-3 justify-center justify-items-center p-10 gap-10 max-lg:flex-col">
    {#each projects as project}
        <ProjectItem project={project}/>
    {/each}
    <AddProject/>
</section>