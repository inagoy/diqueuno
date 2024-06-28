<script>
  import Carrousel from "../components/Carrousel.svelte";
  import Divider from "../components/Divider.svelte"
</script>

<main class="flex flex-col ">
    <section  id="introPage" class="relative flex-grow h-screen items-center justify-center">
      <div class="select-none absolute inset-0 flex items-center justify-center">
        <div class="text-center  text-3xl sm:text-4xl md:text-5xl  z-[2] " style="text-shadow: 2px 2px 10px black">
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
      <div class="flex flex-grow flex-col md:flex-row px-5 md:px-10">
        <div class="md:w-1/3 md:h-full h-1/3">
          <div class="h-full flex items-center justify-center">
            <p class="text-left md:text-right text-white sm:text-lg text-base px-5 lg:pr-10 leading-loose">
              <span class=" text-orange-600 font-semibold">DiqueUNO</span> está ubicada en Ensenada. 
              <br/>A 300 metros de las facultades de Humanidades y Psicología de la Universidad Nacional de La Plata.
              <br/>A su vez se encuentra a 15 minutos a pie del centro de la ciudad de La Plata.
            </p>
          </div>
        </div>
        <div class="md:w-2/3 md:h-full h-2/3 shadow-lg">
          <iframe 
            title="Google Maps"
            src="https://www.google.com/maps/d/embed?mid=1qOKLeB2P5WkwqndK6VP-THtX1bFLJ1M&ehbc=2E312F"
            class="w-full h-full">
          </iframe>
        </div>
      </div>
    </section>
    <section class="border border-blue-400 h-[200px]">
      hola
    </section>
    <section class="border border-yellow-400 h-[200px]">
      hola
    </section>
</main>
