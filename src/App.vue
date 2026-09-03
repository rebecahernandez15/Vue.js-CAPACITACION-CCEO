<!-- v-on se puede acortar con @ -->

<script setup>
const name = "Vue dinámico";

//metodo -methos
const handleClick = (message) =>{
  console.log(message)
}
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <button v-on:click="handleClick('texto 1')">Activame</button>
  <button @click="handleClick('texto 2')">Activame 2</button>
</template>

<style>
h1 {
  color: red;
}
</style>