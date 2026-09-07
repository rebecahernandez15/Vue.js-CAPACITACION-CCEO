<script setup>
import axios from "axios";
import { ref } from "vue";
import { useRoute, useRouter } from "vue-router";

const route = useRoute();
const router = useRouter();
const poke = ref({});

const back = () => {
  router.push('/pokemons');
};

const getData = async () => {
  try {
    const { data } = await axios.get(
        `https://pokeapi.co/api/v2/pokemon/${route.params.name}`
    );
    poke.value = data;
  } catch (error) {
    console.log(error);
  }
};

getData();
</script>

<template>
  <div v-if="poke.sprites">
    <img :src="poke.sprites?.front_default" :alt="poke.name" />
    <h1>Poke name: {{ $route.params.name }}</h1>
    <button @click="back" class="btn btn-outline-primary">Volver</button>
  </div>
</template>