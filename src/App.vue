<script setup>
import {ref, computed} from "vue";

const counter = ref(0);
const numerofavorito = ref([]);
const increment = () => {
  counter.value++;
}
const decrement = () => {
  counter.value--;
}
const reseta = () => {
  counter.value=0;
}
const añadirfavorito = () =>{
  numerofavorito.value.push(counter.value); 
}

const classCounter = computed(() =>{
  if (counter.value ===0 ){
    return 'zero'
  }
  if (counter.value > 0 ){
    return 'positivo'
  }
  if (counter.value < 0){
    return 'negativo'
  }
 
})


</script>

<template>
  <h1> hola </h1>
  <h2 :class="classCounter">{{ counter }}</h2>
 <button @click="increment"> alucoas</button>
 <button @click="decrement"> desencrimentar</button>
 <button @click="reseta"> reseteo</button>
 <button @click="añadirfavorito"> añadir</button>
 <ul>
  <li v-for="number in numerofavorito" :key="number">
{{ number }}
  </li>
 </ul>


 
</template>

<style>
.positivo{
 color: green
}
.negativo{
  color: red
}
.zero{
  color: peru
}
</style>
