<script setup>
import BlogPost from "@/components/BlogPost.vue";
import { ref } from "vue";

const posts = ref([
  { tittle: "Post 1", id: 1, body: "description1" },
  { tittle: "Post 2", id: 2, body: "description2" },
  { tittle: "Post 3", id: 3, body: "description3" },
  { tittle: "Post 4", id: 4 }
]);



const favorito = ref('');

const cambiarFavorito = (tittle) => {
  favorito.value = tittle;
};
</script>

<template>
  <div class="container">
    <h1>APP</h1>
    <h2>Mis Post Favoritos: {{ favorito }}</h2>

    <BlogPost
        v-for="post in posts"
        :key="post.id"
        :tittle="post.tittle"
        :id="post.id"
        :body="post.body"
        @cambiarFavorito="cambiarFavorito"
    ></BlogPost>
  </div>
</template>