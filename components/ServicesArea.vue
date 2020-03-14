<template>
<div class="container mx-auto mt-56">
  <div class="flex flex-col content-center items-center services-area__title-zone">
    <span class="separator"></span>
      <h1 class="font-bold text-2xl md:text-5xl mb-2 capitalize"> Nuestros servicios</h1>
      <h2 class="text-center text-gray-700 mb-8"> Lorem ipsum dolor sit amet, consectetur adipisicing </h2>
  </div>
  <div class="grid col-gap-4 row-gap-4 grid-cols-1 sm:grid-cols-1 md:grid-cols-2 md:text-2xl lg:grid-cols-2  xl:grid-cols-4 services-card-container ">
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
              'Soluciones para el ahorro energético',
              'instalciones electricas en baja tension',
              'iluminación',
              'alumbrado',
              'planos y desarrollos eléctricos'
            ],
          },{
            id: 2,
            src: "/img/solar-panel.svg",
            alt: "imagen paneles solares",
            title: "Paneles Solares",
            features:[
              'instalacion',
              'Suministro',
            ],

          },
          {
            id: 3,
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
          {
            id: 4,
            src: "/img/air-conditioner.svg",
            alt: "imagen calentadores solares",
            title: "Aires Acondicionados",
            features:[
              'instalación.',
              'mantenimiento',
            ],

          },
        ]
      }
    }

  }
</script>

<style scoped>
</style>
