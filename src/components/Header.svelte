<script>
    export let y;
    let tabs = [
       {name: 'Habitaciones', link: '#habitaciones'},
       {name: 'Servicios', link: '#servicios'},
    ]
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-solid'+ (
    y > 0 ? 'py-4 bg-slate-950 border-green-950' : 'py-6 bg-transparent border-transparent'
)}>
    <h1 class="font-medium">
        DiqueUNO
    </h1>
    <div class="sm:flex items-center gap-4 hidden">
        {#each tabs as tab, index}
            <a href={tab.link} class="duration-200 hover:opacity-40">
                <p>{tab.name}</p>
            </a>
        {/each}
    </div>
</header>