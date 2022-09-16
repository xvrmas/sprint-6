<template>
  <div v-if="condition">
    <div
      id="ImatgeFons"
      :style="{ backgroundImage: `url(${llista[seleccionat].img})` }"
    >
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
  data() {},
};
</script>

<style>
body {
  display: grid;
  align-content: center;
  text-align: center;
}
#ImatgeFons {
  background-position: center center;
  background-attachment: fixed;
  background-size:cover ;
  height: 80vh;
  /* width: auto; */
  background-repeat: no-repeat;
}
h4 {
  border: solid;
  background-color: white;
  opacity: 0.7;
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
  opacity: 1;
}
</style>