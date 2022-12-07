<script>
    export let title = "";
    export let subtitle = "";
    export let image_url = "";
    export let archived;
    export let platform = "";
    import IoMdLock from 'svelte-icons/io/IoMdLock.svelte'
    import IoMdDesktop from 'svelte-icons/io/IoMdDesktop.svelte'
    import IoMdPhonePortrait from 'svelte-icons/io/IoMdPhonePortrait.svelte'
</script>

<img src="{image_url}" alt="{title} image" class="aspect-square w-[250px] object-contain">
<div class="flex flex-col justify-center items-center gap-4">
    <p class="text-3xl font-bold">{title}</p>
    <p class="text-l font-bold">{subtitle}</p>
    {#if (archived)}
        <span class="absolute top-4 right-4 w-6 h-6" title="archived"><IoMdLock/></span>
    {/if}
    {#if (platform == 'Website')}
        <span class="w-7 h-7"><IoMdDesktop /></span>
    {:else}
        <span class="w-7 h-7"><IoMdPhonePortrait /></span>
    {/if}
</div>
