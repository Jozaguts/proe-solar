<template>
  <div class="full-width-container " id="mainContainer">
      <div class="grid-container"> <!--hero-->
      <div class="call-to-action-container p-8">
        <h1 class="main-title capitalize">Energía de calidad al alcance</h1>
        <button class="btn btn-call-to ">
        Nuestro Proyectos
        </button>
      </div>
      <div class="form-container p-8">
        <form-component></form-component>
      </div>
    </div><!--end hero-->
      <section class="services-area px-8" ref="servicesArea" id="servicesArea">   <!--services area-->
        <services-area  v-if="servicesArea" class="appear"> </services-area>
      </section>  <!--end services area-->
      <section class="about-area px-8" ref="aboutArea" id="aboutArea">
        <about-area  v-if="aboutArea" :image="aboutImage" class="appear"></about-area>
      </section>
      <section class="last-project-area px-8" ref="lastProjectArea" id="lastProjectArea">
        <last-projects-area   v-if="lastProjectArea" class="appear" ></last-projects-area>
      </section>
  </div>
</template>

<script>
  import FormComponent from "@/components/Form";
  import ServicesArea from "@/components/ServicesArea";
  import AboutArea from "@/components/AboutArea";
  import LastProjectsArea from '../components/LastProjectsArea'
export default {
  components:{
    FormComponent,
    ServicesArea,
    AboutArea,
    LastProjectsArea
  },
  data () {
    return {
      aboutImage:{
        src: '/img/team-worker.jpg',
        alt: 'Imagen de equipo de trabajo'
      },
      servicesArea:false,
      lastProjectArea:false,
      aboutArea:false,
      options: {
        root: null,
        rootMargin: '0px 0px 0px 0px',
        threshold: 1
      },
    }
  },
  methods: {
    showContainer(entries,observer){
      entries.forEach(entry => {
        if(entry.isIntersecting && !this[entry.target.id]){
          this[entry.target.id] = true;
        }
      });
    },

  },
  mounted() {
    const observer = new IntersectionObserver(this.showContainer, this.options)
    for(let element in this.$refs) {
      observer.observe(this.$refs[element])
    }
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
    width: 100%;
  }
  .form-container{
    position: relative;
    z-index: 30;
  }
  .grid-container::before{
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
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto;
    grid-gap: 1rem;
    background-image: url('/img/solar-panels.jpg');
    background-repeat: no-repeat;
    background-position: 50% 50%;
    background-size: cover;
    width: 100%;
    z-index: 30;
  }
  .call-to-action-container {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    position: relative;
    z-index: 30;
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





</style>
