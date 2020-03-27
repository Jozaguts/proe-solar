<template>
    <div class="container mx-auto mt-56">
      <div class="grid col-gap-4 grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-2 xl:grid-cols-2">
        <div class="container mx-auto mb-4 ">
          <img :src="image.src" :alt="image.alt" class="w-full rounded">
        </div>
        <div class="content-container">
          <h1 class="text-3xl mb-4">¿Por qué elegirnos? </h1>
          <p class="text-gray-700 text-justify mb-4">Somos una empresa especializada en la calidad y ahorro energético, contando con personal altamente capacitado. Nos definen:</p>
          <ul class="pb-8 ">
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Calidad y Compromiso</li>
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Profesionalismo</li>
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Vanguardismo</li>
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Accesibilidad</li>
          </ul>
          <button class="bg-info-color text-white px-16 py-4 rounded text-center ">Nosotros</button>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'AboutArea',
    props: ['image']
  }
</script>

<style scoped>

</style>