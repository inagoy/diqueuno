<script>
    import { Card } from 'flowbite-svelte';
    let cards = [
        {
            name: 'Internet-TV',
            text: 'Contamos con servicio de internet de alta velocidad, incluyendo que sea accesible desde todos los rincones de la residencia, incluyendo las habitaciones.',
            icon: 'fa-solid fa-wifi',
        },
        {
            name: 'Lavadero',
            text: 'Contamos con servicio de lavandería de alta calidad, incluyendo que sea accesible desde todos los rincones de la residencia, incluyendo las habitaciones.',
            icon: 'fa-solid fa-tint',
        },
        {
            name: 'Cocina equipada',
            text: 'Contamos con una cocina amplia y equipada con heladeras, microondas, horno y vajillas.',
            icon: 'fa-solid fa-utensils',
        },
        {
            name: 'Limpieza',
            text: 'Contamos con un servicio de limpieza semanal para asistir en el mantenimiento de la limpieza.',
            icon: 'fa-solid fa-trash',
        }
    ]
</script>
<div class="flex flex-grow">
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-4 p-10 opacity-90">
        {#each cards as card}
        <Card class="shadow-2xl bg-gray-100 flex flex-col items-center justify-center">
            <h5 class="mb-2 text-lg md:text-2xl font-semibold text-gray-900 text-center">{card.name}</h5>
            <p class="mt-3 text-sm md:text-base font-normal text-gray-500 dark:text-gray-400 text-center">{card.text}</p>
            <div class="text-center lg:text-9xl md:text-7xl text-5xl mt-5 flex items-center justify-center flex-grow">
                <i class="fa {card.icon} text-primary-600" aria-hidden="true"></i>
            </div>
        </Card>
        {/each}
    </div>
</div>