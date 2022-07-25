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

<style>
body {
  display: grid;
  align-content: center;
  text-align: center;
}

h4 {
  border: solid;
  background-color: rgb(255, 255, 255);
  border-radius: 40px;
  padding: 10px;
}
</style>