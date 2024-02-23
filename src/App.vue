<script setup>
import { ref } from 'vue'

const contador = ref(0)

function decrementar() {
  contador.value--
  if(contador.value < 0){
    contador.value=0
  }
}
function reset() {
  contador.value=0
}
</script>

<template>
<button @click="contador++">+</button>
<button @click="decrementar">-</button>
<button @click="reset">R</button>
<p>O valor do contador é: {{ contador }}</p>
</template>

<style scoped>
button {
  font-size: 2rem;
  padding: 1rem;
  margin: 1rem;
  cursor: pointer;
  border: none;
  background-color: rgb(0, 112, 211);
  border-radius: 0.5rem;
  transition: 0.3s ease-in;
}</style>
