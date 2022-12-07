<script>
    import IoMdLock from 'svelte-icons/io/IoMdLock.svelte'
    export let project;
    import IoMdDesktop from 'svelte-icons/io/IoMdDesktop.svelte'
    import IoMdPhonePortrait from 'svelte-icons/io/IoMdPhonePortrait.svelte'
</script>

<div class="flex flex-col items-center justify-center gap-8 p-6 w-[250px] h-[250px] rounded-xl border-2 border-gray-300 bg-gray-500 hove:border-red-500 hover:bg-red-800 bg-opacity-10 backdrop-blur-lg text-white">
    <p class="text-3xl font-bold">{project.name}</p>
    <p class="text-l font-bold text-center">{project.description}</p>
    {#if (project.isArchived)}
        <span class="absolute top-4 right-4 w-6 h-6" title="archived"><IoMdLock/></span>
    {/if}
    {#if (project.type == 'Website')}
        <span class="w-7 h-7"><IoMdDesktop /></span>
    {:else}
        <span class="w-7 h-7"><IoMdPhonePortrait /></span>
    {/if}

</div>