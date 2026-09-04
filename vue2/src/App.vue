<script setup>
import { ref } from "vue";

import PaginatePost from "./components/PaginatePost.vue";
import BlogPost from "./components/BlogPost.vue";

const posts = ref([]);
const postXpage = 10;
const inicio = ref(0);
const fin = ref(postXpage);

const favorito = ref("");

const cambiarFavorito = (title) => {
  favorito.value = title;
};

const next = () => {
  inicio.value = inicio.value + postXpage;
  fin.value = fin.value + postXpage;
}

const prev = () => {
  //inicio.value = inicio.value + postXpage;
  inicio.value += -postXpage;
  fin.value = -postXpage;
}


fetch("https://jsonplaceholder.typicode.com/posts")
    .then((res) => res.json())
    .then((data) => {
      posts.value = data;
    });
</script>

<template>
  <div class="container">
    <h1>APP</h1>
    <h2>Mis Post Favorito: {{ favorito }}</h2>

    <button @click="next">Next provisorio</button>
    <button @click="prev">Prev provisorio</button>

    <PaginatePost class="mb-2" />

    <BlogPost
        v-for="post in posts.slice(inicio, fin)"
        :key="post.id"
        :title="post.title"
        :id="post.id"
        :body="post.body"
        @cambiarFavorito="cambiarFavorito"
        class="mb-2"
    ></BlogPost>
  </div>
</template>