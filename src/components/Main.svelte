<script>
    import Stats from "./Stats.svelte";
import Step from "./Step.svelte";

    let steps = [
        {
            name: "Pocket ID",
            icon: "fa-solid fa-id-badge",
            href: "https://github.com/stonith404/pocket-id",
            description:
                "Pocket ID is a Simple yet Power OIDC provider that uses Passkeys for authentication. While I'm not the Owner or Creator of Pocket ID, I have contributed to the project, for example the LDAP Sync, and the Docusaurus documentation, and more. This is a project im passionate about and will always help to keep it thriving!",
        },
        {
            name: "This Website",
            icon: "fa-solid fa-code",
            href: "https://github.com/kmendell/svelte-website",
            description:
                "This Website you are currently on, was built from Scratch using SvelteKit and TailwindCSS. This was my first attempt in a long time for building a website, and the first time ever using Tailwind and SvelteKit.",
        },
        {
            name: "My Music",
            icon: "fa-brands fa-spotify",
            href: "https://solo.to/ofkm",
            description:
                "In addition to Programming I also write, record, and produce my own music! You can see the latest release I have dropped at the link below! ",
        },
    ];

    let stats = [
        {
            name: "Github Grade",
        },
        {
            name: "Github Stats",
        },
    ]

    let benefits = [
        {
            metric: "10x",
            name: "a self taught developer",
            description:
                "I taught myself to code using free online resources and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with HTML, Then moving to Visual Basic, then moving to more backend languages like Go, and C.",
        },
        {
            name: "a fast and adaptive learner",
            description:
                "I have been known to learn and grab new concepts and knowledge fast, and consistently, and adapt to the changing aspects of IT, and Technology.",
        },
        {
            name: "an excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships and ensures my effectiveness and productivity in any work space with any team.",
        },
    ];

    function createEmail() {
        window.location.href = "mailto:kmendell@outlook.com";
    }
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-blue-400">Kyle</span> Mendell
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-blue-400"> favorite tech</span> includes <span class="text-blue-400">GoLang</span>, and Ive been learning Svelte, TypeScript, and Node.js as well!
            </p>
            <button
            on:click={createEmail}
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-blue-400 opacity-20 group-hover:translate-x-full z-0 duration-200"></div>
                <h4 class="relative z-9">Email Me &rarr;</h4>
            </button>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img src={"images/kyle.jpg"} alt="Kyle" class="object-cover z-[2] max-h-[40vh] rounded-full" />
        </div>
    </section>
    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>  
                    Pocket ID is a Simple yet Power OIDC provider that uses <strong
                        class="text-blue-400"
                        >Passkeys for authentication.</strong
                    > While I'm not the Owner and Creator of Pocket ID, I have contributed to the project, 
                    for example the LDAP Sync feature, and the Docusaurus documentation, and more. 
                    This is a project im passionate about and will always help to keep it thriving!
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <!-- <div class="z-[-1] bg-blue-950 w-screen left-1/2 -translate-x-1/2 top-0 h-full absolute"> </div> -->
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-blue-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-blue-700 py-4"
        >
            <h6 class="text-large sm:text-xl md:text-2xl">
                Want to know more?
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-blue-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <!-- <div class="flex flex-col gap-2 mx-auto">
                    <div class="flex items-end gap-4">
                        <p
                            class="poppins text-6xl sm:text-7xl md:text-8xl text-slate-500 font-medium"
                        >
                            {benefit.metric}
                        </p>
                        <p
                            class="text-xl sm:text-2xl md:text-3xl capitalize pb-2"
                        >
                            {benefit.name}
                        </p>
                    </div>
                    <p class="text-center italic">- {benefit.description}</p>
                </div> -->
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <!-- <h5 class={" text-2xl sm:text-3xl font-semibold text-center poppins "}>
            The <span class="text-blue-400">Complete</span> Package
        </h5> -->
        <!-- <div
            class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
        >
            <table class="bg-white text-slate-700 rounded text-center">
                <thead class={"border-b border-solid border-slate-200  "}>
                    <tr class="">
                        <th></th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                        <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                        <th
                            class="bg-blue-700 text-white whitespace-nowrap p-4 px-8"
                            >Me</th
                        >
                    </tr>
                </thead>
                <tbody>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Dedication</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-b border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Critical Thought</td
                        >
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr>
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Interpersonal Skills</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                    <tr class="border-t border-solid border-slate-200">
                        <td
                            class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm"
                            >Progamming Ability</td
                        >
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-slate-500"></i></td>
                        <td><i class="fa-solid fa-check text-green-500"></i></td>
                    </tr>
                </tbody>
            </table>
        </div> -->
        <!-- <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
            <p>Scroll to see more &rarr;</p>
        </div> -->
        <section
        id="stats"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl text-center">
            Github <span class="poppins text-blue-400">Stats</span>
        </h2>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-5 lg:gap-10">
            <Stats step={stats[0]}>
                <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kmendell&exclude_repo=tprdp,thinpiproject,thinpi&locale=en&hide_title=false&card_width=320&langs_count=5&theme=transparent&hide_border=true" height="150" alt="languages graph"  />
            </Stats>
            <Stats step={stats[1]}>
                <img src="https://github-readme-stats.vercel.app/api?username=kmendell&hide_title=false&hide_rank=false&show=reviews,discussions_started,discussions_answered,prs_merged&show_icons=true&include_all_commits=true&count_private=true&card_width=320&disable_animations=false&theme=transparent&locale=en&hide_border=true" height="150" alt="stats graph"  />
            </Stats>

        </div>
        </section>
        
    </section>
</main>
