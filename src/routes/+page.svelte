<script>
  import Home from "../components/Home.svelte";
  import Divider from "../components/Divider.svelte";

  
	import Ubicacion from "../components/Ubicacion.svelte";
  import Habitaciones from "../components/Habitaciones.svelte";

</script>

<main class="flex flex-col ">
    <section  id="introPage" class="relative flex-grow h-screen items-center justify-center">
      <Home />
    </section>
    <section id="donde-estamos" class="h-screen flex flex-col bg-gray-800 bg-opacity-60">
      <Divider name="Dónde estamos" id="#donde-estamos" />
      <Ubicacion/>
    </section>
    <section id="habitaciones" class="h-screen flex flex-col bg-gray-800 bg-opacity-60">
      <Divider name="Habitaciones" id="#habitaciones" />
      <Habitaciones/>
    </section>
    <section class="border border-yellow-400 h-[200px]" >
      hola
    </section>
</main>
