<template>
  <div>
    <label>Tarea: </label>
    <input
      type="text"
      placeholder="Ingrese Nueva Tarea"
      v-model="tarea.opcion"
      class="mx-2"
    />
    <button class="btn btn-info" @click="crearTarea">Crear</button>
    <Titulo texto="Lista" class="py-3" />
    <ul>
      <li v-for="(nuevaTarea, index) in nuevasTareas" :key="index">
        {{ index + 1 }}: {{ nuevaTarea.opcion }}
      </li>
    </ul>
  </div>
</template>
<script>
import Titulo from "./Titulo.vue";
export default {
  name: "NuevaTarea",
  components: { Titulo },
  data() {
    return {
      nuevasTareas: [],
      tarea: { opcion: "" },
    };
  },
  methods: {
    crearTarea() {
      this.nuevasTareas.push(JSON.parse(JSON.stringify(this.tarea)));
      this.tarea.opcion = "";
    },
  },
};
</script>

<style>
</style>