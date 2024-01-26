<script setup>
const lista_herramientas = [
    'CSS',
    'GitHub',
    'Git',
    'HTML',
    'JavaScript',
    'MySQL',
    'Python',
    'React',
    'SASS',
    'Tailwind',
    'Vue.js',
    'Node.js'
]
const url = '/img/icons/'
</script>

<template>
    <div class="p-10 bg-gradient-to-r from-slate-900 from-10% via-sky-900 via-40% to-cyan-900 to-100%">
        <h1 class="text-white font-bold text-3xl ">Experiencia y Habilidades</h1>

        <div class="grid lg:grid-cols-4 md:grid-cols-3 grid-cols-2 gap-3 mt-7">
            <div v-for="herramienta in lista_herramientas">
                <div class="flex flex-col items-center gap-3">
                    <img class="w-20 hover:bg-slate-200 rounded-full p-1 transition delay-75" :src="url + herramienta.toLocaleLowerCase() + '.svg'" alt="">
                    <p class="text-white font-bold hover:text-lime-600 transition delay-75">{{ herramienta }}</p>
                </div>
            </div>
        </div>
    </div>
</template>