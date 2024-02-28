<template>
  <div id="app">
    <Contador @numeroClicado="handleNumeroClicado" />
    <p v-if="clickedNumber !== null">Número clicado: {{ clickedNumber }}</p>
  </div>
</template>

<script>
import Contador from './components/Contador.vue';

export default {
  components: {
    Contador,
  },
  data() {
    return {
      clickedNumber: null,
    };
  },
  methods: {
    handleNumeroClicado(numero) {
      this.clickedNumber = numero;
    },
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 60px;
}

p {
  font-size: 18px;
  margin-top: 20px;
}
</style>
