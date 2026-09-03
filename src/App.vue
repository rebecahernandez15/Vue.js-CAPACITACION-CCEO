<!-- v-on se puede acortar con @ -->

<script setup>
const name = "Vue dinámico";

//metodo -methos
const handleClick = () =>{
  console.log('me diste click')
}
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <button v-on:click="handleClick()">Activame</button>
  <button @click="handleClick()">Activame 2</button>
</template>

<style>
h1 {
  color: red;
}
</style>