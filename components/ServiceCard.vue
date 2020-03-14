<template>
    <div class="flex flex-col items-center service-card pb-8">
      <span class="icon-container">
        <img :src="data.src" :alt="data.alt" >
      </span>
      <div class="title-container">
        <h1 class="text-info-color mb-4 font-bold capitalize"v-text="data.title"> </h1>
      </div>
      <div class="content-container text-center px-10">
        <ul class="pb-8">
          <li v-for="feature in data.features"
              :key="feature"
              v-text="feature"
              class="text-white text-left li-text-custom pl-4 text-base leading-loose"
          ></li>
        </ul>
        <div class="btn-container mb-4">
          <button class="btn text-white font-medium bg-info-color px-24 py-4 rounded">Cotiza</button>
        </div>
      </div>
    </div>
</template>

<script>
  export default {
    name: 'ServiceCard',
    props:[
      'data'
    ]
  }
</script>

<style scoped>
  .service-card {
    background: #142E7B;
    background: -webkit-linear-gradient(bottom, #142E7B, #4E56AB);
    background: -moz-linear-gradient(bottom, #142E7B, #4E56AB);
    background: linear-gradient(to top, #142E7B, #4E56AB);
    border-radius: 5px;
  }
.icon-container{
  padding-top: 3rem;
  padding-bottom: 3rem;
  width: 100%;
  max-width: 70px;
}

</style>
