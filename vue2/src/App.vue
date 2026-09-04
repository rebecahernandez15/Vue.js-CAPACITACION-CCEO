<script setup>
import ButtonCounter from "@/components/ButtonCounter.vue";
import BlogPost from "@/components/BlogPost.vue";
import {ref} from  "vue";

const posts = ref([
  { tittle: "Post 1", id: 1, body: "description1" },
  { tittle: "Post 2", id: 2, body: "description2" },
  { tittle: "Post 3", id: 3, body: "description3" },
  { tittle: "Post 4", id: 4, body: "description4" }
]);
</script>

<template>
  <div class="container">
    <h1>APP</h1>
    <buttonCounter/>
    <buttonCounter/>


    <BlogPost
        v-for="post in posts"
        :key="post.id"
        :tittle="post.tittle"
        :id="post.id"
        :body="post.body"
    ></BlogPost>
  </div>
</template>

