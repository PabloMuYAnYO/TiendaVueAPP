<!-- Esto es un ejemplo, crea los componentes con esta estructura -->
<template>
  <div class="hello">
    <!-- Añadimos aquí el html necesario para nuestro componente hijo -->
    <h1>{{ msg }}</h1>   <!-- Añadido desde props:{msg} -->
    <p>
      For a guide and recipes on how to configure / customize this project,<br>
      check out the
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
    </p>
    <h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>Essential Links</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>
  </div>
</template>

<script>
// Componenetes importados a este componente
// import OtroComponente from './components/OtroComponente.vue'
export default { // Funciones, variables, metodos y todo el comportamiento del componente aquí
  name: 'HelloWorld',
  components: { // Usar componenetes importados a este componente
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
    // :\Datos_00\Academia_Grupo_Studio\2º_CURSO_DAW\FRONTEND\DWEC-JS\Ejercicios-Clase-DWEC\Clases\reutilizacion de componentes con props\contadores
    // incrementar(){this.contador+=Number(this.cantidad)},
    // decrementar(){this.contador-=Number(this.cantidad)},
  },
  watch:{ // Vigilar variables
    // Ejemplo en :\Datos_00\Academia_Grupo_Studio\2º_CURSO_DAW\FRONTEND\DWEC-JS\Ejercicios-Clase-DWEC\Clases\Vue Watch\analizador;
    // pregunta(valor){
    //   if(valor.includes('?')){
    //     this.obtenerRespuesta('')
    //   }
    // }
  },
  props: { // Propiedades declaradas aquí
    msg: String
  }
}
</script>

<!-- Agregue el atributo "scoped" para limitar CSS solo a este componente -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

<!-- APUNTES

Crear proyecto vue

> vue create nombreproyecto

Opciones predefinidas
- preset = Manually select features
- features = (*) Babel
- version = 3.x
- linter/formatter = EsLint with error prevention only
- lint features = Lint on save
- config for babel = In dedicated config files
- thi in future projects? = >N

Poco a poco se crearán los archivos necesarios para tu proyecto

Al crearse podrás comprobar que todo esta listo con;

Navegamos a la ruta correspondiente de nuestro proyecto
> cd nombreproyecto

Y iniciamos la vista desde un navegador
>npm run serve

Despues podremos visualizarlo desde  http://localhost:PORT/ o http://192.168.x.x:PORT/
  
-->