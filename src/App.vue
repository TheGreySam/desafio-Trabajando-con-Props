<template>
  <div id="app">
    
    <div id="input">
      <span>Tarea</span>
      <input 
      type="text"
      placeholder="Ingresa nueva tarea"
      v-model="nuevaActividad">
      <button @click="nuevaActividad">Agregar</button>
    </div>
    <h1>Lista</h1>
    <Actividades></Actividades>

    <ul>
      <li>actividad: {{actividad}}</li>
    </ul>
    
  </div>
</template>

<script>
import Actividades from './components/actividades.vue'


export default {
  name: "App",
  data: () => ({
    actividad: "lalala",
    nuevaActividad: "lololo",
    x: 2,
  }),
  components: {
    Actividades,
  },
  method: {

  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  
  margin: 60px;
}

#input {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  
  font-weight: bold;
  
}
</style>
