<script setup>
import {ref, computed} from 'vue'
import Presentacion from '@/components/Presentacion.vue';
import SobreMi from '@/components/SobreMi.vue';
import Proyectos from '@/components/Proyectos.vue';
import Experiencia from '@/components/Experiencia.vue'
import Contacto from '@/components/Contacto.vue'


const visible = ref(false)

const menuHamburgueza = () => {
    if (visible.value === false) {
        visible.value = true
    }else{
        visible.value = false
    }
}

const secciones = (seccion) => {
    
}   


const claseVisible = computed(() => {
    return visible.value === true ? 'block' : 'hidden'
})

</script>

<template>
  <header>
    <nav class="flex items-center justify-between flex-wrap bg-gradient-to-r from-slate-900 from-10% via-sky-900 via-30% to-cyan-900 to-90% p-6">
        <div class="flex items-center flex-shrink-0 text-white mr-6">
            <span class="font-bold text-2xl tracking-tight">Portafolio</span>
        </div>
        <div class="block lg:hidden">
            <button id='boton' @click="menuHamburgueza()"
                class="flex items-center px-3 py-2 border rounded text-teal-200 border-teal-400 hover:text-white hover:border-white">
                <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                    <title>Menu</title>
                    <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                </svg>
            </button>
        </div>
        <div id='menu' class="w-full lg:flex lg:items-center lg:w-auto" :class="claseVisible">
            <div class="text-sm lg:flex-grow">
                <a 
                    href="#home" 
                    class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4 text-xl font-semibold"
                >
                    Home
                </a>
                <a 
                    href="#sobreMi" 
                    class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4 text-xl font-semibold"
                >
                    Sobre mi
                </a>
                <a 
                    href="#portafolio" 
                    class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4 text-xl font-semibold"
                >
                    Portafolio
                </a>
                <a 
                    href="#experiencia" 
                    class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4 text-xl font-semibold"
                >
                    Experiencia
                </a>
                <a 
                    href="#contacto" 
                    class="block mt-4 lg:inline-block lg:mt-0 text-teal-200 hover:text-white mr-4 text-xl font-semibold"
                >
                    Contacto
                </a>
            </div>
    </div>
</nav>
  </header>

  <main class="container-xl ">
    <Presentacion/>
    <section id="sobreMi">
      <SobreMi/>
    </section >
    <section id="portafolio">
      <Proyectos/>
    </section>
    <section id="experiencia">
      <Experiencia/>
    </section>
  </main>

  <footer id="contacto">
    <Contacto/>
  </footer>

</template>
