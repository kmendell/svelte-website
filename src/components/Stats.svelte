<script>
    export let stat;
</script>

<a
    href=" "
    target="_blank"
    class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-blue-700 text-center cursor-pointer group hover:border-blue-400 duration-200"
>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">
        <!-- {stat.name} -->
    </h3>
    <slot />
    <div class="flex-1 flex justify-betweeen gap-4 items-end">
        <div
            class="ml-auto cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:bg-white after:w-full after:h-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden"
        >
        </div>
    </div>
</a>