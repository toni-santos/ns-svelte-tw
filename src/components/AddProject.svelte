<script>
    import { onMount, afterUpdate } from 'svelte';
    import IoIosAdd from 'svelte-icons/io/IoIosAdd.svelte'
    import AddProjectDialog from './AddProjectModal.svelte'

    $: openDialog = false;
    function switchDialog() {
        openDialog = openDialog ? false : true;
        console.log(openDialog);
    }

</script>

<!-- svelte-ignore a11y-click-events-have-key-events -->
<div on:click={() => {switchDialog()}} class="flex flex-col items-center justify-center gap-8 p-6 w-[250px] h-[250px] rounded-xl border-2 border-gray-300 bg-gray-500 hove:border-red-500 hover:bg-red-800 bg-opacity-10 backdrop-blur-lg text-white">
    <span class="w-20 h-20"><IoIosAdd /></span>
</div>
<AddProjectDialog bind:open={openDialog}/>
