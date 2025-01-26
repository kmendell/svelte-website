<script>
    export let y;

    let tabs = [
        {name: 'Projects', link: '#projects'},
        {name: 'About', link: '#about'},
        {name: 'Stats', link: '#stats'},
        // {name: 'Blog', '#projects'},
    ]

    function createEmail() {
        window.location.href = "mailto:kmendell@outlook.com";
    }
</script>

<header
    class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border-b border-solid " +
        (y > 0
            ? " py-4 bg-slate-950 border-blue-950"
            : " py-6 bg-transparent border-transparent")}
>
    <h1 class="font-medium">
        <b class="font-bold poppins">Kyle</b> <span class="">Mendell</span>
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a
                href={tab.link}
                class="duration-200 hover:text-blue-400"
                target={index === 3 ? "_blank" : ""}
            >
                <p>{tab.name}</p>
            </a>
        {/each}
        <button on:click={createEmail}
        class="blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-white text-slate-950"
    >
        <div
            class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
        <h4 class="relative z-9">Contact Me</h4>
    </button>
    </div>
</header>