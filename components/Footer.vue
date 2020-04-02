<template>
  <footer class="container max-w-full bg-info-color">
     <div class="container mx-auto grid md:grid-cols-3 grid-cols-3">
       <div class="flex flex-col m-5">
         <h1 class="text-white font-bold  mb-3">Nosotros</h1>
         <ul>
           <li class=" text-main-dark-color font-medium mb-3">Visión</li>
           <li class=" text-main-dark-color font-medium mb-3">Misión</li>
           <li class=" text-main-dark-color font-medium mb-3">Bolsa de Trabajo</li>
         </ul>
       </div>
        <div class="flex flex-col m-5">
          <h1 class="text-white font-bold  mb-3">Servicios</h1>
          <ul>
            <li class=" text-main-dark-color font-medium mb-3">Paneles Solares</li>
            <li class=" text-main-dark-color font-medium mb-3">Instalaciones Eléctricas</li>
            <li class=" text-main-dark-color font-medium mb-3">Aires Acondicionados</li>
            <li class=" text-main-dark-color font-medium mb-3">Calentadores Solares</li>
          </ul>
        </div>
       <div class="flex flex-col m-5">
          <h1 class="text-white font-bold  mb-3">Contacto</h1>
          <div class="grid grid-cols-3">
            <a href="https://www.facebook.com/PROE-SOLAR-104413387841116" target="_blank">
              <span class="icon icon-facebook"></span>
            </a>
            <a href="">
              <span class="icon icon-whatsapp"></span>
            </a>
            <a href="mailto:solarproe@gmail.com">
              <span class="icon icon-email"></span>
            </a>
          </div>
         <div class="flex mt-5">
              <span class="icon icon-call-us"> </span>
           <div class="flex flex-col">
             <em class="ml-3">322-312-312-31</em>
             <em class="ml-3">322-312-312-31</em>
           </div>
         </div>
        </div>
     </div>
    <div class="foot container mx-auto text-main-dark-color font-bold">
      <h2> &copy; {{date}} ProeSolar.com</h2>
    </div>
  </footer>
</template>
<script>
  export default {
      computed:{
        date(){
          let date = new Date()
            return date.getFullYear();
        }
      }
  }
</script>
<style scoped>
  .icon {
    background-position: 50% 50%;
    width: 50px;
    height: 50px;
    display: block;
    background-size: cover;
    background-repeat: no-repeat;
  }
  .icon:hover{
    cursor: pointer;
  }
  .icon-facebook {
    background-image: url("../assets/Icons/facebook.svg");
  }
  .icon-whatsapp {
    background-image: url("../assets/Icons/whatsapp.svg");
  }
  .icon-email {
    background-image: url("../assets/Icons/correo-electronico.svg");
  }
  .icon-call-us {
    background-image: url("../assets/Icons/telefono.svg");
  }


</style>
