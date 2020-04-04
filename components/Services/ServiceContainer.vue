<template>
  <div >
    <div class="service-container flex flex-col lg:flex-row md:flex-row  "  v-for="(service, index) in services" :key="service.id">
      <div class="img-container lg:w-2/5"   :class="[index % 2  === 0 && $mq != 'sm'? 'order-1' : '']">
        <carousel :nav="false" :responsive="{0:{items:1},768:{items:3}}" >
          <img v-for="img in service.images" :key="img.id" :src="img.src" :alt="img.alt" class="rounded p-2">
        </carousel>
      </div>
      <div class="content-container px-5 lg:w-3/5">
        <h1 class="capitalize text-3xl text-info-color mb-3 font-bold" v-text="service.name"></h1>
        <p class="leading-relaxed text-main-color font-medium" v-text="service.content"></p>
        <hr>
        <button class="rounded bg-info-color text-white font-bold py-2 px-4 my-4 " :class="[index % 2  === 0 ? 'float-right': '']" >Contactar</button>
      </div>
    </div>
  </div>
</template>
<script>
  import carousel from 'vue-owl-carousel';
  export default {
    components:{carousel},
    data(){
      return {
        services:[
          {
            id: 1,
            name: 'Obra Eléctrica',
            images:[
              {
                id:"img-1",
                src: 'https://placeimg.com/200/200/any?1',
                alt: 'lorem ipsu'
              },
              {
                id:"img-2",
                src: 'https://placeimg.com/200/200/any?2',
                alt: 'lorem ipsu'
              },
              {
                id:"img-3",
                src: 'https://placeimg.com/200/200/any?3',
                alt: 'lorem ipsu'
              },
              {
                id:"img-4",
                src: 'https://placeimg.com/200/200/any?4',
                alt: 'lorem ipsu'
              },
            ],
            content: ' Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.\n' +
              '          Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.Lorem ipsum\n' +
              '          dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.'
          },
          {
            id: 2,
            name: 'Paneles Solares',
            images:[
              {
                id:"img-11",
                src: 'https://placeimg.com/200/200/any?1',
                alt: 'lorem ipsu'
              },
              {
                id:"img-22",
                src: 'https://placeimg.com/200/200/any?2',
                alt: 'lorem ipsu'
              },
              {
                id:"img-33",
                src: 'https://placeimg.com/200/200/any?3',
                alt: 'lorem ipsu'
              },
              {
                id:"img-44",
                src: 'https://placeimg.com/200/200/any?4',
                alt: 'lorem ipsu'
              },
            ],
            content: ' Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.\n' +
              '          Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.Lorem ipsum\n' +
              '          dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.'
          },
          {
            id: 3,
            name: 'Aires acondicionados',
            images:[
              {
                id:"img-111",
                src: 'https://placeimg.com/200/200/any?1',
                alt: 'lorem ipsu'
              },
              {
                id:"img-222",
                src: 'https://placeimg.com/200/200/any?2',
                alt: 'lorem ipsu'
              },
              {
                id:"img-333",
                src: 'https://placeimg.com/200/200/any?3',
                alt: 'lorem ipsu'
              },
              {
                id:"img-444",
                src: 'https://placeimg.com/200/200/any?4',
                alt: 'lorem ipsu'
              },
            ],
            content: ' Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.\n' +
              '          Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.Lorem ipsum\n' +
              '          dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.'
          },{
            id: 4,
            name: 'Calentadores Solares',
            images:[
              {
                id:"img-11111",
                src: 'https://placeimg.com/200/200/any?1',
                alt: 'lorem ipsu'
              },
              {
                id:"img-22222",
                src: 'https://placeimg.com/200/200/any?2',
                alt: 'lorem ipsu'
              },
              {
                id:"img-33333",
                src: 'https://placeimg.com/200/200/any?3',
                alt: 'lorem ipsu'
              },
              {
                id:"img-44444",
                src: 'https://placeimg.com/200/200/any?4',
                alt: 'lorem ipsu'
              },
            ],
            content: ' Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.\n' +
              '          Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.Lorem ipsum\n' +
              '          dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.'
          },
          {
            id: 5,
            name: 'Iluminación',
            images:[
              {
                id:"img-111111",
                src: 'https://placeimg.com/200/200/any?1',
                alt: 'lorem ipsu'
              },
              {
                id:"img-2222222",
                src: 'https://placeimg.com/200/200/any?2',
                alt: 'lorem ipsu'
              },
              {
                id:"img-333333",
                src: 'https://placeimg.com/200/200/any?3',
                alt: 'lorem ipsu'
              },
              {
                id:"img-444444",
                src: 'https://placeimg.com/200/200/any?4',
                alt: 'lorem ipsu'
              },
            ],
            content: ' Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.\n' +
              '          Lorem ipsum dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.Lorem ipsum\n' +
              '          dolor sit amet, consectetur adipisicing elit.\n' +
              '          Aliquid commodi, corporis eum magni numquam omnis pariatur porro rem sunt veniam.'
          }
        ]
      }
    }
  }
</script>
<style scoped>
  .service-container {
    box-shadow: 0 4px 28px rgba(0,0,0,0.25), 0 10px 10px rgba(0,0,0,0.22);
    padding: 2rem  1rem;
  }
  hr{
    border-top: 2px solid #bbb;
  }
</style>
