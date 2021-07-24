<template>
  <div id="app">
    <div class="container-fluid col-4 mx-auto my-5">
      <Titulo texto="Crea Una Nueva Tarea" class="pb-3" />
      <NuevaTarea />
    </div>
  </div>
</template>

<script>
import Titulo from "./components/Titulo.vue";
import NuevaTarea from "./components/NuevaTarea.vue";
export default {
  name: "App",
  components: {
    Titulo,
    NuevaTarea,
  },
};
</script>


