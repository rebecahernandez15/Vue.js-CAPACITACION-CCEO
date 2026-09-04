<script setup>
import ButtonCounter from "@/components/ButtonCounter.vue";
import BlogPost from "@/components/BlogPost.vue";
</script>

<template>
  <div class="container">
    <h1>APP</h1>
    <buttonCounter/>
    <buttonCounter/>


    <BlogPost tittle="Post 1"/>
    <BlogPost tittle="Post 2"/>
    <BlogPost tittle="Post 3"/>
    <BlogPost tittle="Post 4"/>
  </div>
</template>

