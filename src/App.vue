<script setup>
import { ref, computed } from 'vue'; // 1. Importamos computed

const name = "Vue dinámico";

const counter = ref(0);
const increment = () => {
  counter.value++;
};

const decrement = () => {
  counter.value--;
};

const reset = () => {
  counter.value = 0;
};

// 2. Corregimos la lógica del computed
const classCounter = computed(() => {
  if (counter.value === 0) {
    return 'zero';
  }
  if (counter.value > 0) { // Corregido: mayor que 0
    return 'positive';
  }
  if (counter.value < 0) {
    return 'negative';
  }
});
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>

  <!-- 3. Vinculamos el computed a la directiva :class -->
  <h2 :class="classCounter">{{ counter }}</h2>

  <button @click="increment()">Aumentar</button>
  <button @click="decrement()">Disminuir</button>
  <button @click="reset()">Resetear</button>
  <button :disabled="false">Add</button>
</template>

<style>
h1 {
  color: red;
}
.positive {
  color: green;
}
.negative {
  color: red;
}
.zero {
  color: peru;
}
</style>