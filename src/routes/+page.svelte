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
    <section id="donde-estamos" class="h-screen flex flex-col">
      <Divider name="Dónde Estamos" id="#donde-estamos"/>
      <div class="flex flex-grow md:flex-row flex-col"> 
        <div class="md:w-1/2 h-full">
          <div class="h-full ">
              
          </div>
        </div>
        <div class="md:w-1/2 h-full shadow-lg ">
          <iframe 
            src="https://www.google.com/maps/d/embed?mid=1qOKLeB2P5WkwqndK6VP-THtX1bFLJ1M&ehbc=2E312F" 
            class=" w-full h-full ">
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
