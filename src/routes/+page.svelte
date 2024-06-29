<script>
  import Carrousel from "../components/Carrousel.svelte";
  import Divider from "../components/Divider.svelte";

  import { Gallery } from 'flowbite-svelte';

  const images = [
    { alt: 'Habitación 1', src: '/images/habitaciones/1.jpg' },
    { alt: 'Pasillo', src: '/images/habitaciones/3.jpg' },
    { alt: 'Habitación 2', src: '/images/habitaciones/2.jpg' },
  ];
</script>

<main class="flex flex-col ">
    <section  id="introPage" class="relative flex-grow h-screen items-center justify-center">
      <div class="select-none absolute inset-0 flex items-center justify-center">
        <div class="text-center  text-3xl sm:text-4xl lg:text-5xl  z-[2] " style="text-shadow: 2px 2px 10px black">
          <!-- <h1 class="font-semibold">Bienvenidos a <span class=" text-orange-600">DiqueUNO</span></h1> -->
          <p>
            <br />Una Residencia exclusiva para <br />
            <span class="text-orange-400 ">Estudiantes Universitarios</span>
          </p>
        </div>
      </div>
      <Carrousel />
    </section>
    <section id="donde-estamos" class="h-screen flex flex-col bg-gray-800 bg-opacity-60">
      <Divider name="Dónde estamos" id="#donde-estamos" />
      <div class="flex flex-grow flex-col lg:flex-row px-5 lg:px-10">
        <div class="lg:w-1/3 lg:h-full h-1/3">
          <div class="h-full flex items-center justify-center opacity-90">
            <p class="text-left lg:text-right text-white  text-sm sm:text-lg px-5 lg:pr-10 sm:leading-loose">
              <span class=" text-orange-400 font-semibold">DiqueUNO</span> está ubicada en Ensenada. 
              <br/>A 300 metros de las facultades de Humanidades y Psicología de la Universidad Nacional de La Plata.
              <br/>A su vez se encuentra a 15 minutos a pie del centro de la ciudad de La Plata.
            </p>
          </div>
        </div>
        <div class="lg:w-2/3 lg:h-full h-2/3 shadow-lg">
          <iframe 
            title="Google Maps"
            src="https://www.google.com/maps/d/embed?mid=1qOKLeB2P5WkwqndK6VP-THtX1bFLJ1M&ehbc=2E312F"
            class="w-full h-full">
          </iframe>
        </div>
      </div>
    </section>
    <section id="habitaciones" class="h-screen flex flex-col bg-gray-800 bg-opacity-60">
      <Divider name="Habitaciones" id="#habitaciones" />
      <div class="flex flex-row overflow-hidden px-[5rem] flex-grow items-center justify-center">
        <Gallery class="gap-2 flex flex-row " items={images} imgClass="rounded-sm object-cover max-h-[30rem] w-full" />
        <div class="flex flex-col justify-center items-center text-sm sm:text-lg sm:leading-loose opacity-90">
          <p class="pl-10 text-justify text-white">
            Nuestras habitaciones son <span class=" text-orange-400 font-semibold">individuales</span> y todas cuentan con:
          </p>
          <ul class="pt-2 text-left">
            <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Ventilación a espacios exteriores</li>
            <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Calefacción eléctrica</li>
            <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Cama</li>
            <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Placard</li>
            <li><i class="fa-solid fa-check pr-2 text-orange-400"></i>Mesa de estudio individual</li>
          </ul>
        </div>
      </div>
    </section>
<!--     <section id="habitaciones" class="h-screen flex flex-col bg-gray-800 bg-opacity-60">
      <Divider name="Habitaciones" id="#habitaciones" />
      <div class="flex flex-grow lg:flex-col px-5 lg:px-10 items-center">
        <div class="h-1/2 md:h-2/3 py-10">
          <Gallery class="h-full gap-2 flex justify-center grid-col-2" items={images} imgClass="h-full rounded-none rounded-sm object-cover" />
        </div>
        <div class="h-1/2 md:h-1/3 md:px-20">
          <p class="text-center text-white text-sm sm:text-lg px-5 lg:pr-10 sm:leading-loose">
            Contamos únicamente con habitaciones individuales. Todas poseen ventilación a expacios exteriores y calefacción eléctrica.
            <br/> Están equipadas con cama, placard y mesa de estudio invididual. 
          <p/>
          <ul class="list-image-none">
            <li>Ventilación a expacios exteriores</li>
            <li>Calefacción eléctrica</li>
            <li>Ventilación a expacios exteriores</li>
            <li>Cama</li>
            <li>Placard</li>
            <li>Mesa de estudio invididual</li>
          </ul>
        </div>
      </div>
    </section> -->
    <section class="border border-yellow-400 h-[200px]" >
      hola
    </section>
</main>
