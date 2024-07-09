<script>
    import { Gallery, Modal } from 'flowbite-svelte';

    const imagesA = [
        { alt: 'Cocina', src: 'images/cocina2.jpg'},
        { alt: 'Fachada', src: '/images/fachada.jpg' },
    ];
    const imagesB = [
        { alt: 'Living', src: '/images/living.jpg' },
        { alt: 'Comedor', src: 'images/comedor2.jpg'},
    ];
    const imagesC = [
        { alt: 'Patio', src: 'images/patio.jpg'},
        { alt: 'Comedor', src: '/images/comedor.jpg' },
    ];
    const imagesD = [
        { alt: 'Cocina', src: '/images/cocina.jpg' },
        { alt: 'Barra', src: '/images/barra.jpg' },
    ];

    

    let currentImg;
    let showModal=false;
    function showPicture(src, alt){
        currentImg= {
            src: src,
            alt : alt,
        }
        showModal=true;
    }
</script>

<div class="flex flex-grow md:px-10">
    <Gallery class="gap-4 grid-cols-2 md:grid-cols-4 py-5">
        <Gallery items={imagesA} let:item >
            <button on:click={showPicture(item.src, item.alt)} class=" hover:opacity-80">
                <img src={item.src} alt={item.alt} class="object-cover h-full" />
            </button>
        </Gallery>
        <Gallery items={imagesB} let:item>
            <button on:click={showPicture(item.src, item.alt)} class=" hover:opacity-80">
                <img src={item.src} alt={item.alt} class="object-cover h-full" />
            </button>
        </Gallery>
        <Gallery items={imagesC} let:item>
            <button on:click={showPicture(item.src, item.alt)} class=" hover:opacity-80">
                <img src={item.src} alt={item.alt} class="object-cover h-full" />
            </button>
        </Gallery>
        <Gallery items={imagesD} let:item>
            <button on:click={showPicture(item.src, item.alt)} class=" hover:opacity-80">
                <img src={item.src} alt={item.alt} class="object-cover h-full" />
            </button>        
        </Gallery>


    </Gallery>
</div>
<Modal 
    bind:open={showModal} 
    size='xl'
    autoclose
    dialogClass='fixed top-0 start-0 end-0 h-modal md:inset-0 md:h-full z-50 w-full flex bg-black bg-opacity-70 '
    footerClass="bg-opacity-0"
    bodyClass='flex-1 '
    class="bg-opacity-0 items-center justify-center rounded-sm"
>
    <div class="object-cover">
        <img src={currentImg.src} alt={currentImg.alt} class="max-h-[500px]"/>
        <h1 class="text-center pt-10 md:text-lg text-base">{currentImg.alt}</h1>
    </div>
</Modal>