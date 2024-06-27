<script>
    import { slide } from 'svelte/transition';
    export let y;
    
    let tabs = [
       {name: 'Habitaciones', link: '#habitaciones'},
       {name: 'Servicios', link: '#servicios'},
    ]

    let menu = false;
</script>


<header class={'fixed w-full z-[10] top-0 transition-all py-6 duration-700 px-6 flex flex-row justify-between ' + (
        y > 0 ? 'bg-orange-800 bg-opacity-60 h-[5rem] ' : ' bg-orange-800 bg-opacity-95 h-[8rem] '
    ) + (menu? '': 'shadow-xl')
}>
    <div class="flex items-center justify-between gap-2">
        <a href="/">
            <img src="/favicon.png" alt="Logo" width="80px" class="cursor-pointer" />
        </a>
        <h1 class="font-medium opacity-80">
            Residencia Estudiantil <b>DiqueUNO</b>
        </h1>
        <div class="absolute sm:hidden right-4 items-center gap-4">
            <button on:click={() => { menu = !menu }} class="ml-auto rounded-sm bg-amber-900 px-3 hover:bg-slate-800 cursor-pointer">
                <i class={"fa-solid grid place-items-center aspect-square my-3 mx-3 " + (menu ? "fa-caret-up" : "fa-caret-down" )}></i>
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
    <div 
        class={"sm:hidden absolute transition-all duration-700 top-full left-0 w-full z-[9] shadow-xl "  + (
            y > 0 ? ' bg-orange-800 bg-opacity-60 ' : ' bg-orange-800 bg-opacity-95 '
          )}
        transition:slide>
        <div class="flex flex-col items-start w-full px-10">
            {#each tabs as tab, index}
            <div class="w-full">
                <a href={tab.link} class="px-4 duration-200 hover:opacity-40">
                    <p>{tab.name}</p>
                </a>
                <hr class="opacity-40"/>
            </div>
            {/each}
            <div class="w-full">
                <a href="#contacto" class="px-4 duration-200 hover:opacity-40">
                    <p>Contactanos</p>
                </a>
            </div>
        </div>
    </div>
{/if}
</header>

