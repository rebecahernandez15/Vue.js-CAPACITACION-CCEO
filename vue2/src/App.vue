<script setup>
import ButtonCounter from "@/components/ButtonCounter.vue";
import BlogPost from "@/components/BlogPost.vue";
</script>

<template>
  <div class="container">
    <h1>APP</h1>
    <buttonCounter/>
    <buttonCounter/>


    <BlogPost tittle="Post 1" :id="1" body="description1" colorText="primary"/>
    <BlogPost tittle="Post 2" :id="2" body="description2" colorText="secondary"/>
    <BlogPost tittle="Post 3" :id="3" body="description3" colorText="success"/>
    <BlogPost tittle="Post 4" :id="4" body="description4" colorText="primary"/>
  </div>
</template>

