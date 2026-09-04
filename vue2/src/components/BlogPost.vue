<script setup>
//defineProps(['tittle','id','body']);

defineProps({
  tittle:String,
  id:Number,
  body:{
    type:String,
    default: "Sin descripcion"
  },
});
</script>

<template>
  <div class="card">
    <div class="card-body">
      <h5 class="card-title">{{id}} - {{tittle}}
      </h5>
      <p> Lorem ipsum dolor sit amet.</p>
    </div>
  </div>
</template>