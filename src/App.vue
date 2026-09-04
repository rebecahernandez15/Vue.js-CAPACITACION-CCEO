<script setup>
import {ref} from 'vue';
const name = "Vue dinámico";


const counter = ref(0);
const increment = () => {
  counter.value ++;
}

const decrement = () =>{
  counter.value --;
}
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2>{{counter}}</h2>
  <button @click="increment()">Aumentar</button>
  
</template>

<style>
h1 {
  color: red;
}
</style>