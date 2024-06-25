<script>
    import { slide } from 'svelte/transition';
    export let y;
    
    let tabs = [
       {name: 'Habitaciones', link: '#habitaciones'},
       {name: 'Servicios', link: '#servicios'},
    ]

    let menu = false;
    $:console.log(menu)
</script>

<header class={'sticky z-[10] top-0 duration-200 px-6 flex flex-col sm:flex-row justify-between' + (
  y > 0 ? ' delay-100 bg-amber-900 bg-opacity-80 py-1 shadow-xl' : ' delay-100 py-6 bg-amber-900 bg-opacity-20'
)}>
    <div class="flex items-center justify-between gap-2">
        <a href="/">
            <img src="/favicon.png" alt="Logo" width="80px" class="cursor-pointer" />
        </a>
        <h1 class="font-medium opacity-80">
            Residencia Estudiantil DiqueUNO
        </h1>
        <div class="sm:hidden flex items-center gap-4">
            <button on:click={() => { menu = !menu }} class="ml-auto rounded-sm bg-amber-900 px-3 hover:bg-slate-800 cursor-pointer">
                <i class={"fa-solid grid place-items-center aspect-square my-3 mx-3 " + (menu? "fa-caret-up" : "fa-caret-down" )}></i>
            </button>
        </div>
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
  {#if menu}
    <div class="sm:hidden flex flex-col items-start w-full mt-4 " transition:slide>
        {#each tabs as tab, index}
        <div class="w-full">
            <a href={tab.link} class=" py-2 px-4 duration-200 hover:opacity-40">
                <p>{tab.name}</p>
            </a>
            <hr class="opacity-40"/>
        </div>
        {/each}
        <a href="#contacto" class="w-full">
            <div class="w-full">
                <a href="#contacto" class=" py-2 px-4 duration-200 hover:opacity-40">
                    <p>Contactanos</p>
                </a>
            </div>
        </a>
    </div>
  {/if}
</header>
