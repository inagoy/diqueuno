<script>
    import { Gallery } from 'flowbite-svelte';
    import { Carousel } from 'flowbite-svelte';
    
    const images = [
        { alt: 'Habitación 1', src: '/images/habitaciones/1.jpg' },
        { alt: 'Pasillo', src: '/images/habitaciones/3.jpg' },
        { alt: 'Habitación 2', src: '/images/habitaciones/2.jpg' },
    ];
</script>
<div class="flex flex-row overflow-hidden px-[3rem] flex-grow items-center justify-center">
  <div class="hidden flex-grow lg:block">
    <Gallery class="gap-2 flex flex-row" items={images} imgClass="rounded-sm object-cover max-h-[800px] w-full" />
  </div>
  <div class="relative flex-grow h-full lg:hidden">
    <Carousel {images} duration="5000" imgClass="h-full object-cover" class=" rounded-none z-[1]" let:Indicators>
      <Indicators class="z-[1]" />
    </Carousel>
  </div>
    <div class="flex flex-col justify-center items-center text-sm lg:text-base sm:leading-loose opacity-90  pl-5 ">
      <p class="text-left text-white">
        Nuestras habitaciones son <span class="text-orange-400 font-semibold">individuales</span> y todas cuentan con:
      </p>
      <ul class="pt-5 text-left">
        <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Ventilación a espacios exteriores</li>
        <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Calefacción eléctrica</li>
        <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Mesa de estudio individual</li>
        <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Cama</li>
        <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Placard</li>
      </ul>
    </div>
</div>