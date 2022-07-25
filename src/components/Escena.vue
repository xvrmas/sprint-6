<template>
  <div v-for="(value, i) in llista" :key="i">
    <h4>{{ value.text }}</h4>
  </div>
</template>


<script>
export default {
  name: "Escena",
  props: ["llista"],
};
</script>