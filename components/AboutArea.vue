<template>
    <div class="container mx-auto mt-56">
      <div class="grid col-gap-4 grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-2 xl:grid-cols-2">
        <div class="container mx-auto mb-4 ">
          <img :src="image.src" :alt="image.alt" class="w-full rounded">
        </div>
        <div class="content-container">
          <h1 class="text-3xl mb-4">¿Por qué elegirnos? </h1>
          <p class="text-gray-700 text-justify mb-4">Lorem ipsum dolor sit amet, consectetur adipisicing elit. A, temporibus! Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dolores, vitae.</p>
          <ul class="pb-8 ">
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Lorem ipsum dolor sit amet Lorem ipsum dolor..</li>
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Lorem ipsum dolor sit amet Lorem ipsum dolor sit amet..</li>
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Lorem ipsum dolor.</li>
            <li class="text-left text-base li-text-custom pl-4 leading-loose">Lorem ipsum dolor Lorem ipsum dolor. sit amet.</li>
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
