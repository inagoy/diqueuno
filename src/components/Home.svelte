<script>
    import { Carousel } from 'flowbite-svelte';
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
  
  <div class="select-none absolute inset-0 flex items-center justify-center">
    <div class="text-center  text-3xl sm:text-4xl lg:text-5xl  z-[2] " style="text-shadow: 2px 2px 10px black">
      <!-- <h1 class="font-semibold">Bienvenidos a <span class=" text-orange-600">DiqueUNO</span></h1> -->
      <p>
        <br />Una Residencia exclusiva para <br />
        <span class="text-orange-400 ">Estudiantes Universitarios</span>
      </p>
    </div>
  </div>
  <div class="h-full place-content-center">
    <Carousel {images} duration="5000" imgClass="h-full object-cover" class="min-h-screen rounded-none z-[1]" let:Indicators disableSwipe=true>
        <Indicators class="z-[1]"/>
    </Carousel>
  </div>