<template>
    <div class="about-container mb-8">
      <header class="flex lg:justify-start lg:items-end md:justify-start md:items-end ">
        <h1 class="banner-title">Nosotros</h1>
      </header>
      <section class="what-is px-4 ">
        <h2 class="font-bold text-main-color text-2xl sm:text-3xl md:text-4xl lg:text-4x1 my-16">¿Qué es Proesolar?</h2>
        <p class="leading-relaxed text-justify">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Vel, veniam.
        </p>
        <p class="text-gray-500 mt-8">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, sint!
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eaque, sint!
        </p>
      </section>
      <div class="mision-vision grid lg:grid-cols-2 md:grid-cols-2 grid-cols-1">
        <section class="vision px-4 shadow-lg">
          <h2 class="font-bold text-main-color text-2xl sm:text-3xl md:text-4xl lg:text-4x1 my-16 lg:text-center">Vision</h2>
          <p class="p-4">Posicionarnos como empresa líder en el sector energético contribuyendo a la mitigación de emisiones CO2, así mismo concientizar a la sociedad de optar por las energías limpias.</p>
        </section>
        <section class="vision px-4 mx-4 shadow-lg">
          <h2 class="font-bold text-main-color text-2xl sm:text-3xl md:text-4xl lg:text-4x1 my-16 lg:text-center">Misión</h2>
          <p class="p-4">Proe Solar Tiene como misión funcionar como empresa de alto nivel en la sección de las energías limpias, ofreciendo un servicio de alta calidad y profesionalismo a un precio accesible. Innovando en la utilización de productos y equipos de última generación. </p>
        </section>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'Nosotros'
  }
</script>

<style scoped>
  header  {
    width: 100%;
    background-image: url("../assets/images/about-header.jpg");
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    max-height: 300px;
    height: 35vh;
  }

.banner-title{
  color: var(--info-color);
  font-weight: bold;
  font-size: 4rem;
  padding: 0 1rem;
}
@media screen and (max-width: 420px) {
  header{
    height: 20vh;
  }
  .banner-title{
    font-size: 2rem;
    color: var(--main-color);
  }
}
</style>
