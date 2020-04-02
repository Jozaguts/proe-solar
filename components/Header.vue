<template>
  <header>
    <nav
      class="flex items-center justify-between flex-wrap bg-info-color p-6  sticky top-0"
    >
      <div class="flex items-center flex-shrink-0 text-white mr-6">
        <figure>
          <img src="/img/logo200x100.png" width="200" height="150" alt="proesolar_logo">
          <figcaption class="text-main-color">Proyectos de obra eléctrica y solares</figcaption>
        </figure>
<!--        <span class="font-semibold text-xl tracking-tight text-main-color">Obra eléctrica  y solares </span>-->
      </div>
      <div class="block lg:hidden">
        <button
          @click="toggleMenu = !toggleMenu"
          class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white"
        >
          <svg
            class="fill-current h-3 w-3"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <title>Menu</title>
            <path v-if="!toggleMenu" d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
            <polygon v-if="toggleMenu"
              id="Combined-Shape"
              points="10 8.58578644 2.92893219 1.51471863 1.51471863 2.92893219 8.58578644 10 1.51471863 17.0710678 2.92893219 18.4852814 10 11.4142136 17.0710678 18.4852814 18.4852814 17.0710678 11.4142136 10 18.4852814 2.92893219 17.0710678 1.51471863 10 8.58578644"
            ></polygon>
          </svg>
        </button>
      </div>
      <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto" :class="toggleMenu ? 'block' : 'hidden'">
        <div class="text-base font-semibold lg:flex-grow">
          <router-link
          to="/"
          class="block mt-4 lg:inline-block lg:mt-0 text-main-dark-color hover:text-white mr-4"
          >
            Home
          </router-link>
          <router-link
          to="/servicios"
          class="block mt-4 lg:inline-block lg:mt-0 text-main-dark-color hover:text-white mr-4">
            Servicios
          </router-link>
          <router-link
          to="/contacto"
          class="block mt-4 lg:inline-block lg:mt-0 text-main-color hover:text-white mr-4"
          >
            Contacto
          </router-link>
          <router-link to="/nosotros"
                       class="block mt-4 lg:inline-block lg:mt-0 text-main-color hover:text-white mr-4"
          >
            Nosotros
          </router-link>
          <router-link to="/proyectos"
                       class="block mt-4 lg:inline-block lg:mt-0 text-main-color hover:text-white"
          >
            Proyectos
          </router-link>
        </div>
        <div>
          <a
            href="tel:3221029376"
            class="btn-contacto flex text-sm px-4 py-2 leading-none border rounded text-main-color border-main-color hover:border-transparent mt-4 lg:mt-0"
            >
            <svg viewBox="0 0 20 20" width="20" height="20" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <g id="phone-icon" stroke="none"  stroke-width="1" fill="#142d7b" fill-rule="evenodd">
                <g id="icon-shape">
                  <path d="M11.1735916,16.8264084 C7.57463481,15.3079672 4.69203285,12.4253652 3.17359164,8.82640836 L5.29408795,6.70591205 C5.68612671,6.31387329 6,5.55641359 6,5.00922203 L6,0.990777969 C6,0.45097518 5.55237094,3.33066907e-16 5.00019251,3.33066907e-16 L1.65110039,3.33066907e-16 L1.00214643,8.96910337e-16 C0.448676237,1.13735153e-15 -1.05725384e-09,0.445916468 -7.33736e-10,1.00108627 C-7.33736e-10,1.00108627 -3.44283713e-14,1.97634814 -3.44283713e-14,3 C-3.44283713e-14,12.3888407 7.61115925,20 17,20 C18.0236519,20 18.9989137,20 18.9989137,20 C19.5517984,20 20,19.5565264 20,18.9978536 L20,18.3488996 L20,14.9998075 C20,14.4476291 19.5490248,14 19.009222,14 L14.990778,14 C14.4435864,14 13.6861267,14.3138733 13.2940879,14.7059121 L11.1735916,16.8264084 Z" id="Combined-Shape"></path>
                </g>
              </g>
            </svg>
            322-102-9376
          </a>
        </div>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data(){
    return {
      toggleMenu: false,
    }
  }
}
</script>

<style scoped>

  .btn-contacto:hover{
    background-color: white;
    color: var(--main-color);
    border-color: transparent;
    transition: all .4s;
    fill: var(--main-color);

  }
  .btn-contacto:hover #phone-icon{
    transition: all .4s;
    fill: var(--main-color);
  }
  .nuxt-link-exact-active {
    color: #F5F5F5;
  }


</style>
