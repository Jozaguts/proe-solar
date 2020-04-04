<template>
  <div class="container mx-auto my-5 grid grid-cols-1" >
  <ServiceContainer></ServiceContainer>
  </div>

</template>

<script>
  import ServiceContainer from '../components/Services/ServiceContainer'
  export default {
    components: {ServiceContainer},
    name: 'servicios',

  }
</script>

<style scoped>

</style>
