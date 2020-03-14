<template>
    <div class="flex flex-col items-center h-full service-card pb-16 ">
      <span class="icon-container">
        <img :src="data.src" :alt="data.alt" >
      </span>
      <div class="title-container">
        <h1 class="text-info-color mb-4 font-bold capitalize "v-text="data.title"> </h1>
      </div>
      <div class="content-container text-center h-full px-10 ">
        <ul class="pb-8">
          <li v-for="feature in data.features"
              :key="feature"
              v-text="feature"
              class="text-white text-left li-text-custom pl-4 text-base leading-loose capitalize"
          ></li>
        </ul>
      </div>
      <div class="btn-container">
        <button class="btn text-white font-medium bg-info-color px-24 py-4 rounded">Cotiza</button>
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
  .btn-container {
    /*position: absolute;*/
    /*bottom: 0;*/
    /*left: 0;*/
    /*right: 0;*/
    /*margin: 0;*/

  }

</style>
