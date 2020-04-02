<template>
  <div>
    <header-component></header-component>
      <nuxt />
    <footer-component></footer-component>
  </div>
</template>
<script>
  import HeaderComponent from '../components/Header'
  import FooterComponent from '../components/Footer'
  export default {
    components:{
      HeaderComponent,
      FooterComponent
    }
  }
</script>

<style></style>
