<template>
  <div v-if="condition">
    <div>
      <div
        v-for="(value, i) in llista"
        :key="i"
        :class="{ focus: i === seleccionat }"
      >
        <h4>{{ value.text }}</h4>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "Escena",
  props: ["llista", "seleccionat", "condition"],
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
button {
  padding: 20px;
  width: 50%;
  font-size: 25px;
}
.focus > h4 {
  background-color: rgb(244, 190, 184);
}
</style>