<script>
    import { Carousel, Indicator } from 'flowbite-svelte';
    export const images = [
      {
        alt: 'Living',
        src: '/images/living.jpg',
      },
      {
        alt: 'Fachada',
        src: '/images/fachada.jpg',
      },
      {
        alt: 'Comedor',
        src: '/images/comedor.jpg',
      },
      {
        alt: 'Barra',
        src: '/images/barra.jpg'
      },
      {
        alt: 'Cocina',
        src: '/images/cocina.jpg'
      },
    ];
  </script>
  
  <div class="h-full place-content-center">
    <Carousel {images} duration="5000" imgClass="h-full object-cover" class="min-h-screen rounded-none z-[1]" let:Indicators>
        <Indicators class="z-[1]"/>
    </Carousel>
  </div>