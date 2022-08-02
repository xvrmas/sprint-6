<template>
  <Botons
    @accio1="selectedItem1"
    @accio2="selectedItem2"
    :condition="condition"
  ></Botons>

  <Escena
    :llista="posts"
    :seleccionat="currentSentence"
    :condition="condition"
  ></Escena>
  <div class="careta" v-if="!condition">
    <h2>Benviguts a la web de formació</h2>
    <br />
    <button class="boto-inici" @click="mostrar">{{ "Iniciar" }}</button>
  </div>
</template>

<script>
import Escena from "@/components/Escena.vue";
import Botons from "@/components/Botons.vue";
export default {
  components: { Escena, Botons },

  data() {
    return {
      posts: [
        {
          text: `El nostre heroi estava surant per l'espai sideral quan a la llunyania va albirar una nau espacial`,
        },
        {
          text: "Sentia curiositat per l'interior de la nau i es va posar a inspeccionar-la. Va arribar a una sala amb dues portes.",
        },
        {
          text: "L'heroi va decidir travessar la porta que el portava a casa",
        },
        {
          text: "Mentrestant, altres herois no van tenir tanta sort en la seva elecció ...",
        },
      ],
      currentSentence: 0,
      condition: false,
    };
  },
  methods: {
    mostrar() {
      this.condition = true;
    },
    selectedItem1() {
      this.currentSentence--;
      if (this.currentSentence < 0) {
        this.currentSentence = 0;
      }
    },
    selectedItem2() {
      this.currentSentence++;
      if (this.currentSentence >= this.posts.length) {
        this.currentSentence = 0;
      }
    },
  },
};
</script>
<style>
.careta {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.boto-inici {
  background-color: salmon;
  color: white;
  border: 0;
  border-radius: 50px;
  width: 200px;
}
.boto-inici:hover {
  background-color: rgb(244, 60, 39);
}
</style>