<script>
    import { Card } from 'flowbite-svelte';
</script>
<div class="flex flex-grow">
    <div class="grid grid-cols-2 lg:grid-cols-4 gap-4 p-10 opacity-90">
        <Card class="shadow-2xl bg-gray-100">
            <h5 class="mb-2 text-2xl font-semibold text-gray-900 text-center">Internet - TV</h5>
            <p class="mt-3 font-normal text-gray-500 dark:text-gray-400">Contamos con servicio de internet de calidad contemplando que sea accesible desde todos los rincones de la residencia, incluyendo las habitaciones.</p>
            <div class="text-center lg:text-9xl md:text-7xl text-5xl mt-2 flex flex-grow items-center justify-center">
                <i class="fa fa-wifi text-primary-600" aria-hidden="true"></i>
            </div>
        </Card>
        <Card class="shadow-2xl bg-gray-100">
            <h5 class="mb-2 text-2xl font-semibold text-gray-900 text-center">Lavadero</h5>
            <p class="mt-3 font-normal text-gray-500 dark:text-gray-400">Contamos con un lavadero para que los residentes puedan utilizarlo para lavar su ropa en el horario que dispongan.</p>
            <div class="text-center lg:text-9xl md:text-7xl text-5xl mt-2 flex flex-grow items-center justify-center">
                <i class="fa fa-tint text-primary-600" aria-hidden="true"></i>
            </div>
        </Card>
        <Card class="shadow-2xl bg-gray-100">
            <h5 class="mb-2 text-2xl font-semibold text-gray-900 text-center">Cocina equipada</h5>
            <p class="mt-3 font-normal text-gray-500 dark:text-gray-400">Contamos con una cocina amplia y equipada con heladeras, microondas, horno y vajillas.</p>
            <div class="text-center lg:text-9xl md:text-7xl text-5xl mt-2 flex flex-grow items-center justify-center">
                <i class="fa fa-cutlery text-primary-600" aria-hidden="true"></i>
            </div>
        </Card>
        <Card class="shadow-2xl bg-gray-100">
            <h5 class="mb-2 text-2xl font-semibold text-gray-900 text-center">Servicio de Limpieza</h5>
            <p class="mt-3 font-normal text-gray-500 dark:text-gray-400">Contamos con un servicio de limpieza semanal para asistir a los residentes en el mantenimiento de la limpieza de la residencia</p>
            <div class="text-center lg:text-9xl md:text-7xl text-5xl mt-2 flex flex-grow items-center justify-center">
                <i class="fa fa-trash text-primary-600" aria-hidden="true"></i>
            </div>
        </Card>
    </div>
</div>