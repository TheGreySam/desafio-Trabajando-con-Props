<template>
    
  <div>
        <ul>
            <li v-for="(actividad, $index) in actividades" :key="$index">
                {{actividad}}
            </li>
            
          
          <button class="btn btn-success" @click="$emit(`eliminar-actividad`, $index)">Eliminar</button>
            
        </ul>
  </div>
    
</template>

<script>

export default {
    name: "Lista",
    props: {
        actividades: { type: Array, required: true},
    }
    
};
</script>

<style scoped>
.input-control {
    display: inline-block;
}
</style>
