<script>

    import Carousel from "svelte-carousel";
    import ProjectItem from './ProjectItem.svelte'
    import SectionHeader from './SectionHeader.svelte'

</script>
<SectionHeader text="Projetos Arquivados"/>
<div class="max-w-[100%] px-[5%] py-10">
    <Carousel>
        <ProjectItem/>
        <ProjectItem/>
        <ProjectItem/>
    </Carousel>
</div>