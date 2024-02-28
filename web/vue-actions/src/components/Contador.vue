<template>
    <div>
      <div v-for="numero in numeros" :key="numero" @click="handleClick(numero)" class="button">
        {{ numero }}
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        numeros: [1, 2, 3, 4, 5, 6, 7, 8, 9],
      };
    },
    methods: {
      handleClick(numero) {
        this.$emit('numeroClicado', numero);
      },
    },
  };
  </script>
  
  <style scoped>
  .button {
    display: inline-block;
    margin: 5px;
    padding: 10px;
    font-size: 18px;
    cursor: pointer;
    background-color: #eee;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  </style>
  