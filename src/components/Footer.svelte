<script>
    import IoLogoFacebook from 'svelte-icons/io/IoLogoFacebook.svelte';
    import IoMdMail from 'svelte-icons/io/IoMdMail.svelte';
    import IoLogoGithub from 'svelte-icons/io/IoLogoGithub.svelte'
    import IoLogoTwitter from 'svelte-icons/io/IoLogoTwitter.svelte';
    import IoLogoLinkedin from 'svelte-icons/io/IoLogoLinkedin.svelte';
    import IoLogoInstagram from 'svelte-icons/io/IoLogoInstagram.svelte';
</script>

<footer class="w-full px-4 pb-2">
    <hr class="my-4 h-px bg-gray-200 border-0">
    <div class="grid grid-cols-3 text-white">
        <div class="flex justify-center flex-row">
            <div class="w-[32px] h-[32px]">
                <IoMdMail />
            </div>
            <div class="w-[32px] h-[32px]">
                <IoLogoGithub />
            </div>
            <div class="w-[32px] h-[32px]">
                <IoLogoTwitter />
            </div>
            <div class="w-[32px] h-[32px]">
                <IoLogoLinkedin />
            </div>
            <div class="w-[32px] h-[32px]">
                <IoLogoFacebook />
            </div>
            <div class="w-[32px] h-[32px]">
                <IoLogoInstagram />
            </div>
        </div>
        <div class="flex justify-center">
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-8 h-8">
                <path stroke-linecap="round" stroke-linejoin="round" d="M4.26 10.147a60.436 60.436 0 00-.491 6.347A48.627 48.627 0 0112 20.904a48.627 48.627 0 018.232-4.41 60.46 60.46 0 00-.491-6.347m-15.482 0a50.57 50.57 0 00-2.658-.813A59.905 59.905 0 0112 3.493a59.902 59.902 0 0110.399 5.84c-.896.248-1.783.52-2.658.814m-15.482 0A50.697 50.697 0 0112 13.489a50.702 50.702 0 017.74-3.342M6.75 15a.75.75 0 100-1.5.75.75 0 000 1.5zm0 0v-3.675A55.378 55.378 0 0112 8.443m-7.007 11.55A5.981 5.981 0 006.75 15.75v-1.5" />
            </svg>
        </div>
        <div class="flex justify-end flex-col text-right pr-10">
            <p>Rua Dr. Roberto Frias 4200-465, Porto</p>
            <p>Sala B315</p>
        </div>
    </div>
</footer>