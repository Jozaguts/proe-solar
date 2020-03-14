<template>
  <div class="container mx-auto mt-56">

      <div class="flex flex-col content-center items-center services-area__title-zone">
        <span class="separator"></span>
        <h1 class="font-bold text-2xl md:text-5xl mb-2 capitalize"> Últimos Proyectos</h1>
        <h2 class="text-center text-gray-700 mb-8"> Lorem ipsum dolor sit amet, consectetur adipisicing </h2>
        <div class="grid col-gap-4 gid-cols-1 sm:grid-cols-1 md-grid-cols-3 lg:grid-cols-3">
          <card-project v-for="data in datum" :key="data.id" :data="data" ></card-project>
        </div>
        </div>

  </div>
</template>

<script>
  import CardProject from './CardProject';
  export default {
    name: 'LastProjectsArea',
    components: {
      CardProject
    },
    data() {
      return {
        datum:[
          {
            id: 1,
            src: "/img/solar-panels-installation.jpg",
            alt: 'Instalación de paneles solares',
            title: 'Instalación de paneles solares ',
            description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.',
            tags: ['#paneles-solares','#instalacion','#energia-renovable ']
          },
          {
            id: 2,
            src: "/img/air-conditioner.jpg",
            alt: 'Imagen de aire acondicionados instalados',
            title: 'Instalación de aire acondicionados en oficinas',
            description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.',
            tags: ['#aire-acondicionado','#instalacion','#oficinas']
          },{
            id: 3,
            src: "/img/water-heater.jpg",
            alt: 'Instalación de calentadores de agua solares',
            title: 'Instalación calentadores de agua',
            description: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.',
            tags: ['#agua','#calentadores-solares','#energia-renovable']
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
