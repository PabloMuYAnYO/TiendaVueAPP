<!-- PADRE -->
<template>
  <section id="padre">
    <!-- Añadimos aquí el html necesario para nuestro componente padre -->
    <producto-vue portada="https://images.unsplash.com/photo-1597763138596-05e6e77e5a5a?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80" titulo="Samsung" :precio="750" :stock="true"></producto-vue>

    <producto-vue portada="https://images.unsplash.com/photo-1615264952739-555010f3b29b?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80
    " titulo="Samsung Galaxy" :precio="850" :stock="true"></producto-vue>

    <producto-vue portada="https://images.unsplash.com/photo-1545947597-7975c1d364eb?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80
    " titulo="Hustle Phone Note" :precio="760" :stock="true"></producto-vue>

    <producto-vue portada="https://images.unsplash.com/photo-1621939703744-9b75e3f7ff0e?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=880&q=80" titulo="Iphone xs" :precio="350" :stock="false"></producto-vue>
  </section>
</template>

<script>
// Componenetes importados a este componente
// import OtroComponente from './components/OtroComponente.vue'
import ProductoVue from './ProductoVue.vue'

export default { // Funciones, variables, metodos y todo el comportamiento del componente aquí
  name: 'TiendaVue',
  components: {
    ProductoVue, // Usar componenetes importados a este componente
    // OtroComponente
  },
  data(){ // Variables usadas aquí
    return{
      // num: 1,
      // texto: 'hola mundo',
      // miArray: [
      //   'ele1',
      //   'ele2',
      //   'ele3'
      // ],
      // aleatorio: Math.floor(Math.random()*3),
    }
  },
  methods:{ // Metodos utilizados

  },
  watch:{ // Vigilar variables

  },
  props: { // Propiedades declaradas aquí

  }
}
</script>

<!-- Agregue el atributo "scoped" para limitar CSS solo a este componente -->
<style scoped>
#padre{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    height: 100vh;

}
</style>