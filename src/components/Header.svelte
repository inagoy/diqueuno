<script>

    export let y;

    let tabs = [
       {name: 'Habitaciones', link: '#habitaciones'},
       {name: 'Servicios', link: '#servicios'},
    ]
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border'+ (
    y > 0 ? 'py-4 bg-amber-900 shadow-xl' : 'py-6 bg-transparent'
)}>
    <div class="flex items-center justify-between gap-2">
        <a href="/">
            <img src="/favicon.png" alt="Logo" width="80px" class="cursor-pointer" />
        </a>
        <h1 class="font-medium opacity-50">
            Residencia Estudiantil DiqueUNO
        </h1>
    </div>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:opacity-40">
                <p>{tab.name}</p>
            </a>
        {/each}
    </div>
</header>