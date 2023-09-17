<template>
  <div class="flex-col items-center">
    <h1 class="text-gray-700 text-6xl">Platzi Exchange v1.0.0</h1>
    <p class="text-gray-600 text-xl text-center">
      Proyecto para obtener las cotizaciones de las cryptomonedas mas
      importantes a traves de la API Rest de Coincap.
      <br />
      Este Proyecto es utilizado en el curso de Vue.js Basico de Platzi
    </p>
    <router-link to="/" class="mt-5 text-xl text-green-600 hover:underline">
      Volver a la pagina de Inicio
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'PxAbout',
}
</script>
