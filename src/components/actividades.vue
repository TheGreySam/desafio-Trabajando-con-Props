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
  

    </div>
</template>

<script>

export default {
    name: "Actividades",
    data: () => ({
        nuevaActividad: "",
        
    }),
    methods: {
        agregarNuevaActividad() {
//            this.actividades.push(this.nuevaActividad)
            this.$emit("nueva-actividad", this.nuevaActividad)
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
