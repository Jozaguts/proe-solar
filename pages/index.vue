<template>
  <div class="full-width-container ">
    <div class="grid-container">
      <div class="call-to-action-container p-8">
        <h1 class="main-title capitalize">Energía de calidad al alcance</h1>
        <button class="btn btn-call-to ">
        Nuestro Proyectos
        </button>
      </div>
      <div class="form-container p-8">
        <form-component></form-component>
      </div>
    </div>
  </div>
</template>

<script>
  import FormComponent from "@/components/Form";
export default {
  components:{
    FormComponent
  }
}
</script>

<style scoped>
*{
  box-sizing: border-box;
}

@media screen and (min-width: 320px) {
  .main-title {
    font-size: 2.5rem;
    color: white;
    font-weight: 600;
  }

  .full-width-container {
    background-image: url('/img/solar-panels.jpg');
    perspective:600px;
    background-repeat: no-repeat;
    background-position: 50% 50%;
    background-size: cover;
    position: relative;
    z-index: 30;
    width: 100%;
  }
  .full-width-container::before{
    content: "";
    display: block;
    position: absolute;
    background-color: black;
    width: 100%;
    height: 100%;
    top:0;
    opacity: .4;
    z-index: 20;
  }
  .grid-container {
    position: relative;
    z-index: 30;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto;
    grid-gap: 1rem;
  }
  .call-to-action-container {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    position: relative;
    animation: appear 1s;
  }
  .btn {
    @apply font-bold py-2 px-4 rounded;
    animation: appear 1.5s;
  }
  .btn-call-to {
    @apply text-white;
    background-color: var(--info-color);
    padding: 1rem;
    font-size: 1.5rem;
    letter-spacing: 1px;
  }
  .btn-call-to:hover {
    background-color: transparent;
    border: 1px solid var(--info-color);
    transition: all .3s;
    color: white;
  }
}
@media screen and (min-width: 768px) {
  .grid-container{
    grid-template-columns: 1fr 1fr;
  }
  .btn {
    margin-top: 1rem;
  }
}
@media screen and (min-width: 1023px) {
  .main-title {
    font-size: 4.5rem;
    color: white;
    font-weight: 600;
  }
  .btn {
    width: 60%;
  }
}


@keyframes appear {
  from{
    opacity: 0;
    transform: translateX(10px);
  }
  to{
    opacity: 1;
    transform: translateX(0px);
  }
}


</style>
