<template>
  <div v-if="condition">
    <button @click="$emit(`accio1`)">Anterior</button>
    <button @click="$emit('accio2')">Següent</button>
  </div>
</template>
<script>
export default {
  name: "Botons",
  props: ["condition"],
  emits: ["accio1", "accio2"],
};
</script>