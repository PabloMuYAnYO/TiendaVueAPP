<template>
  <!-- Añadimos aquí nuestros componentes y otros elementos necesarios -->
  <!-- <hello-world></hello-world> -->
  <tienda-vue></tienda-vue>
</template>

<script>
// Componentes importados a conponente mega padre "App.vue"
//import HelloWorld from './components/HelloWorld.vue'
import TiendaVue from './components/TiendaVue.vue';

export default {
  name: 'App',
  components: {
    TiendaVue
    // HelloWorld

    }
}
</script>

<style>
/* Añadimos aquí estilos globales */
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;  
}
</style>
