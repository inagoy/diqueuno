<script>
  import { onMount } from 'svelte';

  let status = "";
  let name = "";
  let email = "";
  let message = "";
  let showEmptyNameFeedback = false;
  let showEmptyEmailFeedback = false;
  let showInvalidEmailFeedback = false;
  let showEmptyMessageFeedback = false;

  const handleSubmit = async (event) => {
    event.preventDefault();

    if (!validateForm()) {
      return;
    }

    status = 'Enviando...';

    const formData = {
      access_key: "fe5e53de-0edb-4e11-b288-da98aa131352",
      subject: "Mensaje de contacto de la web",
      name,
      email,
      message
    };

    try {
      const response = await fetch("https://api.web3forms.com/submit", {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          Accept: "application/json",
        },
        body: JSON.stringify(formData)
      });

      const result = await response.json();
      if (result.success) {
        status = "¡Mensaje Enviado!";
      } else {
        status = "Ocurrió un error. Intentalo de nuevo.";
      }
    } catch (error) {
      console.error('Error sending message:', error);
      status = "Ocurrió un error. Intentalo de nuevo.";
    }
  };

  const validateForm = () => {
    showEmptyNameFeedback = false;
    showEmptyEmailFeedback = false;
    showInvalidEmailFeedback = false;
    showEmptyMessageFeedback = false;
    let isValid = true;

    if (!name.trim()) {
      showEmptyNameFeedback = true;
      isValid = false;
    }
    if (!email.trim()) {
      showEmptyEmailFeedback = true;
      isValid = false;
    } else if (!isValidEmail(email.trim())) {
      showInvalidEmailFeedback = true;
      isValid = false;
    }
    if (!message.trim()) {
      showEmptyMessageFeedback = true;
      isValid = false;
    }

    return isValid;
  };

  const isValidEmail = (email) => {
    return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
  };

  // Clear status message after 5 seconds
  onMount(() => {
    const clearStatus = setTimeout(() => {
      status = "";
    }, 5000);

    return () => clearTimeout(clearStatus);
  });
</script>

<div class="flex items-center">
  <div class="flex-grow mx-auto">
    <div class="max-w-xl mx-auto mt-10 bg-white bg-opacity-50 p-2 rounded-md shadow-lg">
      <div class="text-center">
        <h1 class="my-3 text-3xl font-semibold text-orange-800">Contactanos</h1>
        <p class="text-gray-800">Llená el formulario para enviarnos un mensaje con tu consulta.</p>
      </div>
      <div class="m-5">
        <form on:submit|preventDefault={handleSubmit} novalidate>
          <div class="flex mb-6 space-x-4">
            <div class="w-full md:w-1/2">
              <label for="full_name" class="block mb-2 text-sm text-gray-800">Nombre completo</label>
              <input type="text" bind:value={name} id="full_name" placeholder="Nombre Apellido" 
                class={"w-full px-3 py-2 placeholder-gray-300 text-gray-800 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300 "  + (showEmptyNameFeedback? 'border-red-400' : '')}
              />
              {#if showEmptyNameFeedback}
                <p class="text-red-900 text-sm mt-1">Ingresá tu nombre completo.</p>
              {/if}
            </div>
            <div class="w-full md:w-1/2">
              <label for="email" class="block mb-2 text-sm text-gray-800">Dirección de email</label>
              <input type="email" bind:value={email} id="email" placeholder="tu@correo.com" 
                class={"w-full px-3 py-2 placeholder-gray-300 text-gray-800 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300 "  + ((showEmptyEmailFeedback||showInvalidEmailFeedback)? 'border-red-400' : '')}
              />
              {#if showEmptyEmailFeedback}
              <p class="text-red-900 text-sm mt-1">Ingresá tu dirección de email.</p>
              {/if}

              {#if showInvalidEmailFeedback}
              <p class="text-red-900 text-sm mt-1">Ingresá una dirección de email válida.</p>
              {/if}
            </div>
          </div>
          <div class="mb-6">
            <label for="message" class="block mb-2 text-sm text-gray-800">Tu mensaje</label>
            <textarea bind:value={message} id="message" rows="5" placeholder="Tu mensaje" 
            class={"w-full px-3 py-2 placeholder-gray-300 text-gray-800 border-2 border-gray-200 rounded-md focus:outline-none focus:ring focus:ring-indigo-100 focus:border-indigo-300 "  + (showEmptyMessageFeedback? 'border-red-400' : '')}
            ></textarea>
            {#if showEmptyMessageFeedback}
              <p class="text-red-900 text-sm mt-1">Ingresá tu mensaje.</p>
            {/if}
          </div>
          <div class="mb-6">
            <button type="submit" 
            class={
              "w-full px-3 py-4 text-white rounded-md " 
              + (status? (
                  status===("Enviando...")|| status===("¡Mensaje Enviado!")? 'bg-green-400 pointer-events-none cursor-not-allowed' : 'bg-gray-400')
                
                : 'bg-orange-400'
                )
            }
          >
          {status? status: "Enviar Mensaje"}</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</div>

<style>
  input:focus, textarea:focus {
    outline: none;
    border-color: #4F46E5;
  }
</style>