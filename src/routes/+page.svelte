<script>
  import Home from "../components/Home.svelte";
  import Divider from "../components/Divider.svelte";
  import Fotos from "../components/Fotos.svelte";
	import Ubicacion from "../components/Ubicacion.svelte";
  import Habitaciones from "../components/Habitaciones.svelte";

</script>

<main class="flex flex-col">
    <section  id="introPage" class="relative flex-grow h-screen items-center justify-center">
      <Home />
    </section>
    <section id="donde-estamos" class="flex flex-col min-h-screen bg-gray-800 bg-opacity-60">
      <Divider name="Dónde estamos" id="#donde-estamos" />
      <Ubicacion/>
    </section>
    <section id="habitaciones" class="flex flex-col min-h-screen bg-gray-800 bg-opacity-60">
      <Divider name="Habitaciones" id="#habitaciones" />
      <Habitaciones/>
    </section>
    <section id="fotos" class="flex flex-col min-h-screen bg-gray-800 bg-opacity-60">
      <Divider name="Fotos" id="#fotos" />
      <Fotos/>
    </section>
</main>
