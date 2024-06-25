<script>

    export let y;

    let tabs = [
       {name: 'Habitaciones', link: '#habitaciones'},
       {name: 'Servicios', link: '#servicios'},
    ]
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border'+ (
    y > 0 ? 'py-4 bg-amber-900 shadow-xl py-2' : 'bg-transparent py-6'
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
    
        <a href="#contacto">
            <button
                class="blueShadow relative overflow-hidden mx-2 px-2 py-2 group rounded-md bg-amber-100 bg-opacity-50 text-slate-950"
                >
                <div
                    class="absolute top-0 right-full w-full h-full bg-amber-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                    <h4 class="relative z-9">Contactanos</h4>
                    
            </button>
        </a>
</div>
</header>