<template>
    <div>
        <div class="input-control d-flex p-2 l-2">
    
    <label class="fs-4">Tarea  </label>
    
    <input class="form-control"
    type="text" 
    placeholder="Ingrese nueva tarea"
    v-model="nuevaActividad">
    <button class="btn btn-primary" @click="agregarNuevaActividad">Agregar</button>
  </div>
        <ul>
          <label>{{nuevaActividad}}</label>
          <button class="btn btn-success">Eliminar</button>
            
        </ul>

    </div>
</template>

<script>

export default {
    name: "Actividades",
    data: () => ({
        nuevaActividad: "",
        actividades: ["Pagar Internet", "Pagar Netflix"]
    }),
    methods: {
        agregarNuevaActividad() {
            this.actividades.push(this.nuevaActividad)
            this.nuevaActividad = "";
        },
        destruirActividad() {
            this.$$destroy
        }
    }
    
    
};
</script>

<style scoped>
.input-control {
    display: inline-block;
}
</style>
