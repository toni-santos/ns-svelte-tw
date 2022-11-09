<script>
    export let title = "";
    export let subtitle = "";
    export let image_url = "";    
</script>

<img src="{image_url}" alt="{title} image" class="aspect-square w-[250px] h-[250px]">
<div class="flex flex-col justify-center items-center gap-4">
    <p class="text-3xl font-bold">{title}</p>
    <p class="text-l font-bold">{subtitle}</p>
</div>
