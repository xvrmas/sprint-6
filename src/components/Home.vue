<template>
  <Botons
    @accio1="selectedItem1"
    @accio2="selectedItem2"
    :condition="condition"
  ></Botons>
  <Escena :llista="posts" :seleccionat="currentSentence"></Escena>
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
    };
  },
  methods: {
    selectedItem1() {
      this.currentSentence--;
    },
    selectedItem2() {
      this.currentSentence++;
    },
  },
};
</script>
<style>
</style>