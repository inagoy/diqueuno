<script>
    import { Gallery, Modal } from 'flowbite-svelte';

    const images = [
        { alt: 'Habitación 1', src: '/images/habitaciones/1.jpg' },
        { alt: 'Pasillo', src: '/images/habitaciones/3.jpg' },
        { alt: 'Habitación 2', src: '/images/habitaciones/2.jpg' },
        { alt: 'Barra', src: '/images/barra.jpg' },
        { alt: 'Fachada', src: '/images/fachada.jpg' },
        { alt: 'Living', src: '/images/living.jpg' },
        { alt: 'Comedor', src: '/images/comedor.jpg' },
        { alt: 'Cocina', src: '/images/cocina.jpg' },
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
    <Gallery class="gap-4 grid-cols-2 md:grid-cols-4" items={images} let:item>
        <button on:click={showPicture(item.src)}>
            <img src={item.src} alt={item.alt} class="h-auto max-w-full" />
        </button>
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
    </div>
</Modal>