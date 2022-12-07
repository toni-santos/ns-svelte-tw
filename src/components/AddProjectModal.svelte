<script>
    import { onMount, afterUpdate } from "svelte";

    export let open;

    function switchModal() {
        console.log("hi");
        if (open) {
            document.querySelector("#modal").showModal();
            open = false;
        } else {
            document.querySelector("#modal").close();
        }
    }

    onMount(switchModal);
    afterUpdate(switchModal);

    async function createProject() {
        const res = await fetch( "https://parseapi.back4app.com/classes/Project", {
                method: "POST",
                body: JSON.stringify({
                    name: "UNI",
                    description: "A FEUP no teu bolso",
                    type: "Aplicação Mobile",
                    imageURL:
                        "https://play-lh.googleusercontent.com/947VgiC4ySPiJtqMxhTDP7XuZs4UTWDtVYBsergfzM4XTbLA7mS4Xrh2lksZ28bm4nrQ=w240-h480",
                }),
                headers: {
                    'X-Parse-Application-Id': 'yB953MbsVE0hvNYJLy9Udleb7uF0bwB4AWDoAuD9',
                    'X-Parse-REST-API-Key': '3TA8ugnSSIN1TB8tQNDGTudYk00i9dghfwloy84c'
                }
            }
        );
    }
</script>

<dialog id="modal" aria-modal="true" class="shadow-lg bg-red-900 rounded-lg border-1 w-[400px]">
    <form method="POST" class="flex flex-col text-white justify-center items-center gap-5">
        <div class="flex flex-col gap-2 w-full justify-center items-center">
            <label for="name" class="text-lg">Name</label>
            <input type="text" name="name" id="name" placeholder="Project Name" class="w-[50%] bg-[#471010] text-white rounded" />
        </div>
        <div class="flex flex-col gap-2 w-full justify-center items-center">
            <label for="name" class="text-lg">Description</label>
            <input type="text" name="description" id="description" placeholder="Project Description" class="w-[50%] bg-[#471010] text-white rounded" />
        </div>
        <div class="flex flex-row justify-evenly gap-20">
            <div>
                <input type="checkbox" id="computer" name="computer" />
                <label for="computer" class="text-lg">Computer</label>
            </div>
            <div>
                <input type="checkbox" id="mobile" name="mobile" />
                <label for="mobile" class="text-lg">Mobile</label>
            </div>
            <div>
                <input type="checkbox" id="archive" name="archive" />
                <label for="archive" class="text-lg">Archived</label>
            </div>
        </div>
        <button type="submit" on:click={createProject()} class="text-lg border-1 rounded px-4 py-1 bg-[#471010]"> Create Project </button>
    </form>
</dialog>
