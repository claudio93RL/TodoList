<template>
  <div>
    <h1 class="titulo">{{ texto }}</h1>
  </div>
</template>

<script>
export default {
  name: "Titulo",
  props: {
    texto: String,
  },
};
</script>

<style>
.titulo {
  color: grey;
}
</style>