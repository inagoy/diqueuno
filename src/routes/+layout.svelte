<script>
    import "../app.css";
    import Footer from "../components/Footer.svelte";
    import Header from "../components/Header.svelte";
    import { Carousel } from 'flowbite-svelte';
    
    const images = [
        { alt: 'Habitación 1', src: '/images/habitaciones/1.jpg' },
        { alt: 'Pasillo', src: '/images/habitaciones/3.jpg' },
        { alt: 'Habitación 2', src: '/images/habitaciones/2.jpg' },
    ];
    let y;
    let innerHeight = 0;
    let innerWidth = 0;

    function goTop(){
        document.body.scrollIntoView()
    }
</script>
<div class="relative flex flex-col mx-auto w-full text-sm sm:text-base min-h-screen">
    <div class={`fixed bottom-0 right-0 duration-200 flex p-10 z-10 ${y > 0 ? 'opacity-100 pointer-events-auto' : 'pointer-events-none opacity-0'}`}>
        <button on:click={goTop} class="rounded-sm bg-amber-900 px-3 hover:bg-slate-800 cursor-pointer shadow-lg">
            <i class="fa-solid fa-arrow-up grid place-items-center aspect-square my-3 mx-3"></i>
        </button>
    </div>
    <Header y={y} />
    <slot />
    <Footer />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth></svelte:window>