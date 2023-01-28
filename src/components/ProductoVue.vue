<!--  HIJO -->
<template>
    <section :id="disponible" class="producto">
      <!-- Añadimos aquí el html necesario para nuestro componente hijo -->
      <img :src="portada">
      <h1>{{ titulo }}</h1>
      <h2> {{ precio }} €</h2>
      <h3>{{ stock }}</h3>
      <div>
        <button @click="decrementar">-</button>
        <span>{{ cantidad }}</span>
        <button @click="incrementar">+</button>
      </div>
      <div>
        <h2>{{ total }} 🤑</h2>
      </div>
    </section>
  </template>

<script>
// Componentes importados a este componente
// import OtroComponente from './components/OtroComponente.vue'

export default { // Funciones, variables, métodos y todo el comportamiento del componente aquí
  name: 'productoVue',
  components: { // Usar componentes importados a este componente
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
      cantidad: 0,
      total: 0,
      disponible: '',
    }
  },
  methods:{ // Métodos utilizados
    incrementar(){
        this.cantidad++ 
        this.total = this.precio * this.cantidad
    },
    decrementar(){
        this.cantidad-- 
        this.total = this.precio * this.cantidad
    },
  },
  watch:{ // Vigilar variables
    cantidad(valor){
      if(valor < 0){
        this.cantidad = 0
        this.total = 0
        // alert('¿Vas a comprar en negativo?')
      }
    }
  },
  props: { // Propiedades declaradas aquí
    portada: String,
    titulo: String,
    precio: Number,
    stock: Boolean,
  },
  mounted(){ // Hook que se ejecuta nada más renderizar e incluir el componente en el DOM 
    if(this.stock==false){
      this.disponible='disponible'
    }
  },
}
</script>

<style scoped>
.producto{
    margin: 1rem;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 20%;
    border-radius: 10px;
    background: #F5DEB3;
    box-shadow: 5px 5px 5px #000000;
}
.producto img{width: 100%; padding: 1rem;}
button{
    padding: .5rem 1.3rem;
    border: none;
    border-radius: 10px;
    background: greenyellow;
    color: #fff;
    font-size: 18px;
    cursor: pointer;
    transition: .4s;
}
button:hover{ background: #00ff00;}
span{ margin: 0 2rem; font-size: 30px;}
.producto div{
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 1rem;
}
#disponible{
  filter: saturate(0);
}
</style>