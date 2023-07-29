<script setup>
import {ref} from "vue";
const counter = ref(0);
const increment = () => {
  counter.value++;
}
const decrement = () => {
  counter.value--;
}
const reseta = () => {
  counter.value=0;
}

</script>

<template>
  <h1> hola </h1>
  <h2 :class="counter > 0 ? 'positivo' : 'negativo'"> {{ counter }}</h2>
 <button @click="increment"> alucoas</button>
 <button @click="decrement"> desencrimentar</button>
 <button @click="reseta"> reseteo</button>
</template>

<style>
.positivo{
 color: green
}
.negativo{
  color: red
}

</style>
