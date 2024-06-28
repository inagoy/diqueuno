<script>
    export let name, id;
</script>
<a href={id}>
    <div class="h-[10rem] bg-gray-800 bg-opacity-80 shadow-lg flex-col items-center justify-center pl-[5rem] z-[2]">
        <h1 class="pt-[6rem] select-none font-medium opacity-80 text-3xl sm:text-4xl" >{name}</h1>
        <hr class="opacity-100"/>
    </div>
</a>