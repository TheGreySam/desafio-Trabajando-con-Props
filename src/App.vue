<template>
  <div>
    <h3>Hola que hace</h3>

    <div>
      <label for=""></label>
      <input 
      type="text"
      placeholder="Agregar"
      v-model="nuevaActividad">
      <button @click="nuevaActividad">Agregar</button>
    </div>
    <h1>Lista</h1>
    <Actividades></Actividades>>

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
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
