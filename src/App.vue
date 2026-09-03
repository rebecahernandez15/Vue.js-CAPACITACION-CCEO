<!-- modificadores  -->

<script setup>
const name = "Vue dinámico";

//metodo -methos
const handleClick = (message) =>{
  console.log(message)
}
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <button v-on:click.right.prevent="handleClick('texto rigth')">Activame rigth</button>
  <button @click="handleClick('texto left')">Activame left</button>
  <button @click.middle="handleClick('texto middle')">Activame middle</button>
</template>

<style>
h1 {
  color: red;
}
</style>