<script>
    import { Carousel, Indicator } from 'flowbite-svelte';
    export const images = [
      {
        alt: 'Cosmic timetraveler',
        src: '/living2.jpg',
        title: 'cosmic-timetraveler-pYyOZ8q7AII-unsplash.com',
      },
      {
        alt: 'Cristina Gottardi',
        src: '/living1.jpg',
        title: 'cristina-gottardi-CSpjU6hYo_0-unsplash.com',
      },
      {
        alt: 'Johannes Plenio',
        src: '/fachada.jpg',
        title: 'johannes-plenio-RwHv7LgeC7s-unsplash.com',
      },
    ];
  </script>
  
  <div class="h-full place-content-center">
    <Carousel {images} duration="5000" imgClass="h-full object-cover" class="min-h-screen rounded-none" let:Indicators>
        <Indicators class="z-[1]"/>
    </Carousel>
  </div>