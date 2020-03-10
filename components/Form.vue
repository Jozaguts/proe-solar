<template>
  <form class="w-full max-w-lg bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4 mx-auto">
    <div class="md:flex md:items-center mb-6 flex-col ">
      <p class="text-gray-700 text-4xl font-bold ">
        Cotiza en linea
      </p>
      <p class="text-gray-500 text-base">
        Es indispensable para la cotización una fotografía o archivo de tu recibo de luz
      </p>
    </div>

    <div class="md:flex md:items-center mb-6">
      <div class="md:w-1/3">
        <label class="block text-gray-700 font-bold md:text-right mb-1 md:mb-0 pr-4" >
          Nombre
        </label>
      </div>
      <div class="md:w-2/3">
        <input v-model="nombre"  class="custom-input bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white" type="text" placeholder="Jane Doe">
      </div>
    </div>
    <div class="md:flex md:items-center mb-6">
      <div class="md:w-1/3">
        <label class="block text-gray-700 font-bold md:text-right mb-1 md:mb-0 pr-4" >
          Correo Electrónico
        </label>
      </div>
      <div class="md:w-2/3">
        <input v-model="correo" class="custom-input bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white" type="email" placeholder="JDoe@example.com">
      </div>
    </div>
    <div class="md:flex md:items-center mb-6">
      <div class="md:w-1/3">
        <label class="block text-gray-700 font-bold md:text-right mb-1 md:mb-0 pr-4" >
          Teléfono
        </label>
      </div>
      <div class="md:w-2/3">
        <input v-model="tel" class="custom-input bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white" type="tel" placeholder="333-333-22-22">
      </div>
    </div><div class="md:flex md:items-center mb-6">
      <div class="md:w-1/3">
        <label class="block text-gray-700 font-bold md:text-right mb-1 md:mb-0 pr-4" >
          Recibo de luz
        </label>
      </div>
      <div class="md:w-2/3">
        <input @change="recibo" class="custom-input bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white"  type="file" accept="image/*,.pdf" capture="camera">
      </div>
    </div>

    <div class="md:flex md:items-center">
      <div class="md:w-1/3"></div>
      <div class="md:w-2/3">
        <button class="shadow info-bg-color hover:bg-purple-400 focus:shadow-outline focus:outline-none text-white font-bold py-2 px-4 rounded" type="button">
          Cotizar
        </button>
      </div>
    </div>
  </form>
</template>

<script>
  export default {
    name: 'Form',
    data(){
      return {
        nombre:"",
        tel: "",
        correo: "",
        recibo: "",
      }
    }
  }
</script>

<style scoped>
  form{
    animation: appear 1.7s;
  }
  .custom-input:focus{
    border-color: var(--info-color);
  }
  .info-bg-color{
    background-color: var(--info-color);
  }
  @keyframes appear {
    from{
      opacity: 0;
      transform: translateY(30px);
    }
    to{
      opacity: 1;
      transform: translateY(0px);
    }
  }
</style>
