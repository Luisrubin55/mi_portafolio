<script setup>
import MainNav from '@/components/MainNav.vue';
import Presentacion from '@/components/Presentacion.vue';
import SobreMi from '@/components/SobreMi.vue';
import Proyectos from '@/components/Proyectos.vue';
import Experiencia from '@/components/Experiencia.vue'
import Contacto from '@/components/Contacto.vue'

</script>

<template>
  <MainNav/>

  <main class="container-xl ">
    <Presentacion/>
    <section>
      <SobreMi/>
    </section>
    <section>
      <Proyectos/>
    </section>
    <section>
      <Experiencia/>
    </section>
  </main>

  <footer>
    <Contacto/>
  </footer>

</template>
