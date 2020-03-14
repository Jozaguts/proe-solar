<template>
<div class="container mx-auto services-area">
  <div class="flex flex-col content-center items-center services-area__title-zone">
    <span class="separator"></span>
      <h1 class="font-bold text-2xl md:text-5xl mb-2"> Lorem ipsum dolor. </h1>
      <h2 class="text-center text-gray-700 mb-8"> Lorem ipsum dolor sit amet, consectetur adipisicing </h2>
  </div>
  <div class="grid col-gap-4 grid-cols-1 sm:grid-cols-1 md:grid-cols-1 md:text-2xl lg:grid-cols-3  xl:grid-cols-3 services-card-container px-4">
    <div class="services-card-container__service" v-for="servicio in servicios">
      <service-card  :key="servicio.id" :data="servicio"> </service-card>
    </div>
  </div>
</div>
</template>

<script>
  import ServiceCard from './ServiceCard';
  export default {
    name: 'ServicesArea',
    components: {
      ServiceCard
    },
    data() {
      return {
        servicios: [
          {
            id: 1,
            src: "/img/power-plant.svg",
            alt: "icono obras eléctrica",
            title: "Obra eléctrica",
            features:[
              'Lorem ipsum dolor.',
              'Lorem ipsum dolor sit amet.',
              'Lorem ipsum dolor sit amet, consectetur.',
              'Lorem ipsum.'
            ],

          },{
            id: 1,
            src: "/img/solar-panel.svg",
            alt: "imagen paneles solares",
            title: "Paneles Solares",
            features:[
              'Lorem ipsum dolor.',
              'Lorem ipsum dolor sit amet.',
              'Lorem ipsum dolor sit amet, consectetur.',
              'Lorem ipsum.'
            ],

          },{
            id: 1,
            src: "/img/heater.svg",
            alt: "imagen calentadores solares",
            title: "Calentadores Solares",
            features:[
              'Lorem ipsum dolor.',
              'Lorem ipsum dolor sit amet.',
              'Lorem ipsum dolor sit amet, consectetur.',
              'Lorem ipsum.'
            ],

          },
        ]
      }
    }

  }
</script>

<style scoped>
  .services-area{
    padding-top: 100px;
    padding-bottom: 50px;
  }

</style>
