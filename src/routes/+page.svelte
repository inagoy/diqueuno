<script>
  import Carrousel from "../components/Carrousel.svelte";
</script>

<main class="flex flex-col ">
    <section  id="introPage" class="relative flex-grow h-screen items-center justify-center">
      <div class="select-none absolute inset-0 flex items-center justify-center">
        <div class="text-center  text-4xl sm:text-5xl md:text-6xl  z-[2] " style="text-shadow: 1px 1px 10px black">
          <!-- <h1 class="font-semibold">Bienvenidos a <span class=" text-orange-600">DiqueUNO</span></h1> -->
          <p>
            <br />Una Residencia exclusiva para <br />
            <span class="text-orange-400">Estudiantes Universitarios</span>
          </p>
        </div>
      </div>
      <Carrousel />
    </section>
    <section class="border border-green-400 h-[200px]">
      hola
    </section>
    <section class="border border-blue-400 h-[200px]">
      hola
    </section>
    <section class="border border-yellow-400 h-[200px]">
      hola
    </section>
</main>
