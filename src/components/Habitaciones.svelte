<script>
    import { Gallery } from 'flowbite-svelte';
    import { Carousel } from 'flowbite-svelte';
    
    const images = [
        { alt: 'Habitación 1', src: '/images/habitaciones/1.jpg' },
        { alt: 'Pasillo', src: '/images/habitaciones/3.jpg' },
        { alt: 'Habitación 2', src: '/images/habitaciones/2.jpg' },
    ];
</script>

<div class="flex flex-grow sm:flex-row flex-col">
  <div class="flex flex-grow lg:hidden items-center">
    <div class="flex-1 flex-grow">
      <Carousel {images} class="min-h-[500px] rounded-sm" imgClass="object-contain max-h-[900px] w-full" let:Controls>
        <Controls class="z-[1]"/>
      </Carousel>
    </div>
  </div>
  <div class="flex-grow hidden lg:flex items-center justify-center pl-10">
    <div class="flex-1 flex-grow">
      <Gallery class="gap-2 flex flex-row items-center" items={images} imgClass="rounded-sm object-cover max-h-[800px] w-full" />
    </div>
  </div>
  <div class="sm:w-1/3 pt-10 sm:pt-0 flex flex-col justify-center items-center text-sm lg:text-base sm:leading-loose opacity-90 px-10">
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