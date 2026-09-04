<script setup>
defineProps({
  tittle: String,
  id: Number,
  body: {
    type: String,
    default: "Sin descripcion"
  }
});

const emit = defineEmits(['cambiarFavorito']);
</script>

<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">{{ id }} - {{ tittle }}</h5>
      <p>{{ body }}</p>


      <button
          @click="emit('cambiarFavorito', tittle)"
          class="btn btn-outline-primary"
      >
        Favorito
      </button>
    </div>
  </div>
</template>